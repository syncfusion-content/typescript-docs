---
layout: post
title: Getting Started | TimePicker | TypeScript | Syncfusion
description: Getting Started
platform: TypeScript
control: TimePicker
documentation: ug
---

# Getting Started

This section explains you how to render and configure TimePicker component in a TypeScript application.

## Create your first TimePicker	

* Create a TypeScript application and refer the dependent modules, script and CSS with the help of given [Getting started documentation](https://help.syncfusion.com/js/typescript).

* In the index.HTML file, add the input element for rendering TimePicker component as given below.

{% highlight html %}

        <input id="timepick" />

{% endhighlight %} 

* Create app.ts file and use the below content

{% highlight JS %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    $(function () {
        var sample = new ej.TimePicker($("#datetimepick"));
    });

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

    tsc

{% endhighlight %} 

Now build your application, so that the app.ts file will compiled and automtically generated the app.js file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file by compiling build the aplication.

Execution of above code will render the following output.

![](Getting-Started_images/Getting-Started_img1.png) 

### Configuring Properties

## DisableTimeRanges

This property specifies the list of time range to be disabled in TimePicker control. To know more about TimePicker properties please refer the [API reference] (https://help.syncfusion.com/api/js/ejtimepicker) documentation.

{% highlight JS %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module TimePickerComponent {
        $(function () {
            var sample = new ej.TimePicker($("#timepick"), { disableTimeRanges: [{ startTime: "3:00 AM", endTime: "6:00 AM" },
                        { startTime: "1:00 PM", endTime: "3:00 PM" },
                        { startTime: "8:00 PM", endTime: "10:00 PM" }]});
        });
    }   

{% endhighlight %}

The following screenshot illustrates the output of above code.

![](Getting-Started_images/Getting-Started_img3.png) 
