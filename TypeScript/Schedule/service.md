---
layout: post
title: Service reference for ejSchedule widget
description: Services referred for Essential JavaScript Scheduler control.
platform: typescript
control: schedule
documentation: ug
keywords: schedule services, schedule exporting services
---
# Scheduler Services

Essential Scheduler makes use of specific service actions which are described below - in order to fetch records from the remote server and bind to it, to export it wholly in a PDF format and also to export/import its appointment content in an ICS format. It makes use of ejDataManager, in order to bind the remote data to it.

## Binding Scheduler data
{:#members:schedule-binding-scheduler-data}

### Description

Fetch and bind the records from *DefaultSchedules* table to the Scheduler.

### URL

[http://js.syncfusion.com/ejservices/api/Schedule/LoadData/](http://js.syncfusion.com/ejservices/api/Schedule/LoadData/)

### Parameter

<table>
    <tr>
        <td>$top</td>
        <td>10</td>
    </tr>
    <tr>
        <td>CurrentAction</td>
        <td>Load</td>
    </tr>
    <tr>
        <td>CurrentDate</td>
        <td>Mon May 05 2014 05:00:00 GMT 0530 (India Standard Time)</td>
    </tr>
    <tr>
        <td>CurrentView</td>
        <td>week</td>
    </tr>
</table>

### Request

{% highlight javascript %}

var dataManger = new ej.DataManager({
    url: "http://js.syncfusion.com/ejservices/api/Schedule/LoadData/"
});

{% endhighlight %}

#### Action getting invoked in C Sharp

{% highlight c# %}

public IEnumerable<DefaultSchedule> GetScheduleData()
{
    var data = new ScheduleDataEntities().DefaultSchedules.ToList();
    return data;
}

{% endhighlight %}

### Response

#### Status Code: 200 OK

#### Content-Type: application/json; charset=utf-8

#### Response (JSON)

{% highlight js %}

[ {"Id":100,"Subject":"Bering Sea Gold","Location":"chennai","StartTime":"2014-05-02T09:00:00","EndTime":"2014-05-02T10
:30:00","Description":null,"Owner":1,"Priority":null,"Recurrence":1,"RecurrenceType":null,"RecurrenceTypeCount"
:null,"Reminder":null,"Categorize":"1,2","CustomStyle":null,"AllDay":false,"RecurrenceStartDate":null
,"RecurrenceEndDate":null,"RecurrenceRule":"FREQ=DAILY;INTERVAL=2;COUNT=10","StartTimeZone":null,"EndTimeZone"
:null},
{"Id":101,"Subject":"Bering Sea Gold","Location":"mum","StartTime":"2014-05-02T04:00:00","EndTime"
:"2014-05-02T05:00:00","Description":null,"Owner":1,"Priority":null,"Recurrence":0,"RecurrenceType":null
,"RecurrenceTypeCount":null,"Reminder":null,"Categorize":"2","CustomStyle":null,"AllDay":false,"RecurrenceStartDate"
:null,"RecurrenceEndDate":null,"RecurrenceRule":null,"StartTimeZone":null,"EndTimeZone":null},

//... 14 more records
]

{% endhighlight %}

## ICS Export Service

### Description

To export appointment data from Scheduler into an ICS file format.

### URL

[http://js.syncfusion.com/ejservices/api/Schedule/IcsExport/](http://js.syncfusion.com/ejservices/api/Schedule/IcsExport) - To export Scheduler appointments in ICS format.

### Parameters

<table>
    <tr>
        <td>ScheduleApps</td>
        <td>{"id":"Id","subject":"Subject","description":"Description","startTime":"StartTime","endTime":"EndTime","recurrence":"Recurrence","recurrenceRule":"RecurrenceRule","allDay":"AllDay","categorize":null,"recurrenceId":"RecurrenceId","recurrenceExDate":"RecurrenceExDate","location":"Location","priority":null,"startTimeZone":"StartTimeZone","endTimeZone":"EndTimeZone"}</td>
    </tr>
    <tr>
        <td>ScheduleModel</td>
        <td>{"views":["day","week","workweek","month","agenda"], ...} -- Schedule Model Values</td>
    </tr>
</table>

### ICS Export Request

{% highlight javascript %}

var obj = $("#Schedule1").data("ejSchedule"); // instance of Scheduler widget after initialization
obj.exportSchedule("http://js.syncfusion.com/ejservices/api/Schedule/IcsExport", null, null); // client-side method to be made use in order to invoke the service action for exporting.

{% endhighlight %}

#### Export Action invoked in C Sharp

{% highlight c# %}

public void IcsExport()
{
    IEnumerable data;
    string JSONModel = HttpContext.Current.Request.Form["ScheduleApps"];
    var model = JsonConvert.DeserializeObject<Dictionary<string, object>>(JSONModel);
    var Id = HttpContext.Current.Request.Form["AppointmentId"];
    var DataSource = new ScheduleDataEntities().DefaultSchedules.ToList();
    if (Id != null)
        data = DataSource.Where(app => app.Id.ToString() == Id.ToString()).ToList();
    else
        data = DataSource.ToList();
    ScheduleExport obj = new ScheduleExport(model, data);
}

{% endhighlight %}

### Response

#### Status Code: 200 OK

#### Content-Type: text/Calendar

## ICS Import Service

### Description

To import appointment data generated from external calendar into Scheduler.

### URL

[http://js.syncfusion.com/ejservices/api/Schedule/Save/](http://js.syncfusion.com/ejservices/api/Schedule/Save) - To import appointments from external ICS files into Scheduler.

### Import Request using Uploadbox externally

{% highlight javascript %}

$("#UploadDefault").ejUploadbox({
    saveUrl: "http://js.syncfusion.com/ejservices/api/Schedule/Save",
    extensionsAllow: ".ics",
    height: "31px",
    autoUpload: true,
    width: "80px",
    buttonText: {
        browse: "Import"
    },
    showFileDetails: false,
    success: "onComplete",
    dialogAction: {
        closeOnComplete: true,
    }
});

{% endhighlight %}

#### Import Action invoked in C Sharp

{% highlight c# %}

public IEnumerable Save()
{
    var files = HttpContext.Current.Request.Files;
    var destinationPath = "";
    try
    {
        for (int i = 0; i < files.Count; i++)
        {
            var fileName = Path.GetFileName(files[i].FileName);
            destinationPath = Path.Combine(HttpContext.Current.Server.MapPath("~/App_Data"), fileName);
            files[i].SaveAs(destinationPath);
        }
    }
    catch (Exception ex) { throw ex; }
    ScheduleImport importApps = new ScheduleImport();
    List<ScheduleImport.ScheduleAppointment> app = importApps.renderingImportAppointments(destinationPath);
    try
    {
        if (File.Exists(destinationPath))
        {
            File.Delete(destinationPath);
        }
    }
    catch (Exception ex) { throw ex; }
    var dataSource = new ScheduleDataEntities().DefaultSchedules.ToList();
    int intMax = dataSource.Max(a => a.Id);
    for (var i = 0; i < app.Count; i++)
    {
        app[i].Id = intMax + 1;
        DefaultSchedule row = new DefaultSchedule();
        row.Subject = app[i].Subject;
        row.AllDay = app[i].AllDay;
        row.Categorize = app[i].AppointmentCategorize;
        row.Description = app[i].Description;
        row.EndTime = Convert.ToDateTime(app[i].EndTime);
        row.Id = app[i].Id;
        row.Location = app[i].Location;
        row.Owner = app[i].Owner;
        row.Recurrence = (!String.IsNullOrEmpty(app[i].RecurrenceRules)) ? Convert.ToByte("1") : Convert.ToByte("0");
        row.RecurrenceRule = app[i].RecurrenceRules;
        row.Reminder = app[i].Reminder;
        //row.Priority = Convert.ToInt32(app[i].Priority);
        row.StartTime = Convert.ToDateTime(app[i].StartTime);
        dataSource.Add(row);
        intMax = app[i].Id;
    }
    return dataSource;
}

{% endhighlight %}

### Response

#### Status Code: 200 OK

#### Content-Type: application/xml; charset=utf-8

## PDF Export Service

### Description

To export the entire Scheduler content in a PDF file format.

### URL

[http://js.syncfusion.com/ejservices/api/Schedule/PdfExport/](http://js.syncfusion.com/ejservices/api/Schedule/PdfExport)

### Parameters

<table>
    <tr>
        <td>ScheduleApps</td>
        <td>{"id":"Id","subject":"Subject","description":"Description","startTime":"StartTime","endTime":"EndTime","recurrence":"Recurrence","recurrenceRule":"RecurrenceRule","allDay":"AllDay","categorize":null,"recurrenceId":"RecurrenceId","recurrenceExDate":"RecurrenceExDate","location":"Location","priority":null,"startTimeZone":"StartTimeZone","endTimeZone":"EndTimeZone"}</td>
    </tr>
    <tr>
        <td>ScheduleProcessedApps</td>
        <td>[{"Id":504,"Subject":"Case study","StartTime":"2014-05-01T18:30:00.000Z","EndTime":"2014-05-03T18:29:00.000Z","Description":"","AllDay":true,"Recurrence":false,"AppTaskId":26,"ParentId":26,"Guid":"557984d8-55de-6a63-3868-f236ad1d2d61","RecurrenceId":null,"RecurrenceExDate":null}, ... ] -- Processed Appointment data</td>
    </tr>
    <tr>
        <td>ScheduleModel</td>
        <td>{"views":["day","week","workweek","month","agenda"], ...} -- Schedule Model Values</td>
    </tr>
</table>

### PDF Export Request

{% highlight javascript %}

var obj = $("#Schedule1").data("ejSchedule"); // instance of Scheduler widget after initialization
obj.exportSchedule("http://js.syncfusion.com/ejservices/api/Schedule/PdfExport", null, null); // client-side method to be made use in order to invoke the service action for exporting.

{% endhighlight %}

#### Export Action invoked in C Sharp

{% highlight c# %}

public void PDFExport()
{
    JavaScriptSerializer serializer = new JavaScriptSerializer();
    SchedulePDFExport convert = new SchedulePDFExport();
    ScheduleProperties scheduleObject = convert.ScheduleSerializeModel(HttpContext.Current.Request.Form["ScheduleModel"]);
    IEnumerable scheduleAppointments = (IEnumerable)serializer.Deserialize(HttpContext.Current.Request.Form["ScheduleProcessedApps"], typeof(IEnumerable));
    PdfExport exp = new PdfExport();
    PdfPageSettings pageSettings = new PdfPageSettings(50f);
    pageSettings.Orientation= PdfPageOrientation.Landscape;
    PdfDocument document = exp.Export(scheduleObject, scheduleAppointments, ExportTheme.FlatAzure, HttpContext.Current.Request.Form["locale"], pageSettings);
    document.Save("Schedule.pdf", HttpContext.Current.Response, HttpReadType.Save);
}

{% endhighlight %}

### Response

#### Status Code: 200 OK

#### Content-Type: application/pdf
