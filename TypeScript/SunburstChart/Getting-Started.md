---
layout: post
title: Getting Started for Essential JavaScript SunburstChart
description: How to create a SunburstChart.
platform: ts
control: SunburstChart
documentation: ug
---

# Getting Started

This section explains you the steps required to populate the Sunburst Chart with data, data labels, legend and title. This section covers only the minimal features that you need to know to get started with the Sunburst Chart.

## Create Sunburst Chart

You can easily create the Sunburst Chart widget by using the following steps.

### Add Libraries

1.First create an TypeScript Project and add the following script reference in the app.ts page 
For common getting started of TypeScript , you can refer [here](https://help.syncfusion.com/js/typescript).

The default type definition file **ej.web.all.d.ts** needs to include the support for type-checking while initializing any of the Syncfusion widgets. 

The important step you need to do is to copy the ej.web.all.d.ts file into your project and then need to refer it in your TypeScript application (app.ts file), so that you will get the intelliSense support and also the compile time type-checking.

You can find the ej.web.all.d.ts file in the following location,

(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\typescript

Apart from ej.web.all.d.ts file, it is also necessary to make use of the **jquery.d.ts** file in your TypeScript application, which can be downloaded from [here](https://github.com/DefinitelyTyped/DefinitelyTyped).

2.Add the following script reference in the HTML page  

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
</head>
<body>
</body>
</html>
{% endhighlight %}
In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/# "") utility to generate a custom script file with the required widgets for deployment purpose.

## Populate Data source:
The datasource for the Sunburst Chart is populated as a JSON object. The “default_data” contains the JSON data for rendering the Sunburst Chart as shown in the sample.

{% highlight js %}

var default_data = [

{ Category: "Employees", Country: "USA", JobDescription: "Sales", JobGroup: "Executive", EmployeesCount: 50 },
{ Category: "Employees", Country: "USA", JobDescription: "Sales", JobGroup: "Analyst", EmployeesCount: 40 },
{ Category: "Employees", Country: "USA", JobDescription: "Marketing", EmployeesCount: 40 },
{ Category: "Employees", Country: "USA", JobDescription: "Technical", JobGroup: "Testers", EmployeesCount: 55 },
{ Category: "Employees", Country: "USA", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Windows", EmployeesCount: 175 },
{ Category: "Employees", Country: "USA", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Web", EmployeesCount: 70 },
{ Category: "Employees", Country: "USA", JobDescription: "Management", EmployeesCount: 40 },
{ Category: "Employees", Country: "USA", JobDescription: "Accounts", EmployeesCount: 60 },

{ Category: "Employees", Country: "India", JobDescription: "Technical", JobGroup: "Testers", EmployeesCount: 43 },
{ Category: "Employees", Country: "India", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Windows", EmployeesCount: 125 },
{ Category: "Employees", Country: "India", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Web", EmployeesCount: 60 },
{ Category: "Employees", Country: "India", JobDescription: "HR Executives", EmployeesCount: 70 },
{ Category: "Employees", Country: "India", JobDescription: "Accounts", EmployeesCount: 45 },

{ Category: "Employees", Country: "Germany", JobDescription: "Sales", JobGroup: "Executive", EmployeesCount: 30 },
{ Category: "Employees", Country: "Germany", JobDescription: "Sales", JobGroup: "Analyst", EmployeesCount: 40 },
{ Category: "Employees", Country: "Germany", JobDescription: "Marketing", EmployeesCount: 50 },
{ Category: "Employees", Country: "Germany", JobDescription: "Technical", JobGroup: "Testers", EmployeesCount: 40 },
{ Category: "Employees", Country: "Germany", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Windows", EmployeesCount: 65 },
{ Category: "Employees", Country: "Germany", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Web", EmployeesCount: 27 },
{ Category: "Employees", Country: "Germany", JobDescription: "Management", EmployeesCount: 33 },
{ Category: "Employees", Country: "Germany", JobDescription: "Accounts", EmployeesCount: 55 },

{ Category: "Employees", Country: "UK", JobDescription: "Technical", JobGroup: "Testers", EmployeesCount: 45 },
{ Category: "Employees", Country: "UK", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Windows", EmployeesCount: 96 },
{ Category: "Employees", Country: "UK", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Web", EmployeesCount: 55 },
{ Category: "Employees", Country: "UK", JobDescription: "HR Executives", EmployeesCount: 60 },
{ Category: "Employees", Country: "UK", JobDescription: "Accounts", EmployeesCount: 30 },

{ Category: "Employees", Country: "France", JobDescription: "Technical", JobGroup: "Testers", EmployeesCount: 40 },
{ Category: "Employees", Country: "France", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Windows", EmployeesCount: 65 },
{ Category: "Employees", Country: "France", JobDescription: "Technical", JobGroup: "Developers", JobRole: "Web", EmployeesCount: 27 },
{ Category: "Employees", Country: "France", JobDescription: "Marketing", EmployeesCount: 50 }

 ];

{% endhighlight %}

## Initialize Sunburst Chart

1. Add a **div** element that acts as a container for **SunburstChart** widget.

{% highlight html %}

<body>
    <div id="Sunburst"></div>
</body>


{% endhighlight %}

2.Initialize the Sunburst Chart in ts file by using the ej.SunburstChart method.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SunburstComponent {
    $(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"));               
      });
}

{% endhighlight %}

3. Now, bind the default_Datasource to `datasource` property of the Sunburst Chart. The`levels`property determines the number of hierarchical levels. Each hierarchy level is formed based on the property specified in `groupMemberPath`property, and each arc segment size is calculated using `valueMemberPath`.

{% highlight javascript %}

module SunburstComponent {
    
$(function () {
var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            dataSource: default_data,
            valueMemberPath: "EmployeesCount",
            levels: [
			{ groupMemberPath: "Country" },
            { groupMemberPath: "JobDescription" },
            { groupMemberPath: "JobGroup" },
            { groupMemberPath: "JobRole" }
            ],
        });               
      });
}

{% endhighlight %}

3. The final HTML file appears as follows

{% highlight html %}

<body>
    <div id="Sunburst"></div>
</body>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module  sunburstComponent {
    $(function () {
        var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
          dataSource: default_DataSource,
                valueMemberPath: "EmployeesCount",
                levels: [
                { groupMemberPath: "Country" },
                { groupMemberPath: "JobDescription" },
                { groupMemberPath: "JobGroup" },
                { groupMemberPath: "JobRole" }
                ],

        });
    });
}

{% endhighlight %}

## Add Title to the Sunburst Chart

The title of the Sunburst chart is used to provide quick information to the user about the data being plotted in the Sunburst Chart. You can add it by using the `text` property of the `title`



{% highlight javascript %}

$(function () {
var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
         title:{text:"Employees Count"},	

            // ...

        });
    });


{% endhighlight %}

## Enable Legend

You can enable or disable the legend by using the `visible` property present inside the `legend`

{% highlight javascript %}

$(function () {

var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
         legend:{visible:true ,position:"left"},	

            // ...

        });
    });


{% endhighlight %}

## Add Data Labels

The data labels are used to improve the readability of the Sunburst chart. This can be achieved by enabling the `visible` property in the `dataLabelSettings`.

{% highlight javascript %}

$(function () {
var sample = new ej.datavisualization.SunburstChart($("#Sunburst"),{
            // ...
         dataLabelSettings:{visible:true},	

            // ...

        });
    });



{% endhighlight %}

Now the Sunburst Chart is rendered along with the specified customizations

![](Getting-Started_images/Getting-Started_img1.png)


