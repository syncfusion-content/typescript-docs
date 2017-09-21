---
title: Getting started with Schedule component
description: Rendering a basic Scheduler
platform: Typescript
control: schedule
documentation: ug
keywords: ejschedule, schedule, schedule widget, js schedule
---

# Getting Started

To get start with how to create a general Typescript application and use Syncfusion widgets within it, refer [here](https://help.syncfusion.com/js/typescript#getting-started). To know more about the Scheduler individual script references, refer [here](/typescript/schedule/dependencies).

## Create an HTML File

Create a new HTML file and include the below initial code.

{% highlight html %}

<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title> </title>
    </head>
    <body>
    </body>
</html>

{% endhighlight %}

## Script/CSS References

Refer the CSS file from the specific theme folder to your HTML file within the `head` section. Refer the built-in available themes from [here](https://help.syncfusion.com/js/theming-in-essential-javascript-components).

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Schedule</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
</head>

{% endhighlight %}

Add links to the [CDN](/js/cdn) Script files of the other required external dependencies.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Schedule</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="app.js"></script>
</head>

{% endhighlight %}

N> Uncompressed version of library files are also available which is used for development or debugging purpose and can be generated from the custom script [here](http://csg.syncfusion.com).

N> The content of `app.js` file reference in the above script section is automatically generated from the `app.ts` file, when the typescript application is compiled.

## Define Container to render Scheduler

Create a `div` element within the body section of the HTML document, where the Scheduler needs to be rendered.

{% highlight html %}

<body>
    <div id="Schedule1"></div>
</body>

{% endhighlight %}

## Control Initialization

Create a typescript module in `app.ts` file with the control initialization code for rendering the scheduler control in its container namely `Schedule1` created through the HTML file. Before the module creation, make sure to refer the `ej.web.all.d.ts` and `jquery.d.ts` type-definition files in your project in order to support the typescript rendering.

{% highlight ts %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var dManager = [{
            Id: 1,
            Subject: "Bering Sea Gold",
            StartTime: new Date(2014, 4, 5, 5, 30),
            EndTime: new Date(2014, 4, 5, 7, 30),
            Description:"",
            AllDay: false,
            Recurrence: false
        }];
        var sample = new ej.Schedule($("#Schedule1"), {
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                description: "Description",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });
}

{% endhighlight %}

Now build your application, so that the `app.js` file is automatically generated from the above typescript file and got added to your project. Now, whatever code changes that you make in `app.ts` file will be reflected in `app.js` file automatically on every successful compilation.

## Setting TimeZone

Initially, the system timezone is preferred as the Schedule's default timezone. When some specific timezone is explicitly defined to the Schedule, it will be set to it.

Likewise, we can also set different timezones for the appointments. Usually, the system timezone is assigned as the appointment's default timezone and it will be positioned on the Scheduler based on the start/end time range and timezone assigned to it.

To set Scheduler timeZone and its appointment timeZone values, refer the below code example -

{% highlight ts %}

/// <reference path="jquery.d.ts" />
/// <reference path="ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var dManager = [{
            Id: 1,
            Subject: "Bering Sea Gold",
            StartTime: new Date(2014, 4, 5, 5, 30),
            StartTimeZone: "UTC +02:00",
            EndTime: new Date(2014, 4, 5, 7, 30),
            EndTimeZone: "UTC +02:00",
            Description:"",
            AllDay: false,
            Recurrence: false
        }];
        var sample = new ej.Schedule($("#Schedule1"), {
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            timeZone: "UTC +05:30",
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                startTimeZone: "StartTimeZone",
                endTime: "EndTime",
                endTimeZone: "EndTimeZone",
                description: "Description",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });
}

{% endhighlight %}