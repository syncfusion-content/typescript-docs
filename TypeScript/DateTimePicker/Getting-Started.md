---
layout: post
title: Getting Started | DateTimePicker | TypeScript | Syncfusion
description: Getting Started
platform: TypeScript
control: DateTimePicker
documentation: ug
---

# Getting Started

This section discloses the details on how to render and configure a DateTimePicker component in a TypeScript application.

## Create your first DateTimePicker	

* Create a TypeScript application and refer the dependent modules, script and CSS with the help of given [getting started document](https://help.syncfusion.com/js/typescript).

* In the index.HTML file, add the input element for rendering DateTimePicker component as given below.

{% highlight html %}

     <input id="datetimepick" />

{% endhighlight %} 

* Create app.ts file and use the below content

{% highlight JS %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    $(function () {
        var sample = new ej.DateTimePicker($("#datetimepick"));
    });

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

    tsc

{% endhighlight %} 

Now build your application, so that the app.ts file will compiled and automtically generated the app.js file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file by compiling build the aplication.

Execution of above code will render the following output.

![](Getting-Started_images/datetime.png) 

### Configuring DateTimePicker

EJ DateTimePicker provides API through which you can set the maximum and minimum allowed date and time values. Min and Max date and time values can be set at initialization as show below.

{% highlight JS %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module DateTimePickerComponent {
        $(function () {
            var sample = new ej.DateTimePicker($("#datetimepick"), { minDateTime: new Date("11/1/2016 10:00 AM"), maxDateTime: new Date("11/27/2016 10:00 PM")});
        });
    }

{% endhighlight %}

The following screenshot illustrates the output of above code.

![](getting-started_images/minmax.png) 