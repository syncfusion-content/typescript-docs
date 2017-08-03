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

1. Create a TypeScript application and refer the dependent modules, script and CSS with the help of given Getting started document.

2. In the index.HTML file, add the input element for rendering TimePicker component as given below.

{% highlight html %}

        <input id="timepick" />

{% endhighlight %} 

3. Create a TypeScript file named "app.ts" file and refer the required definition files as given below.

{% highlight JS %}

        /// <reference path="tsfiles/jquery.d.ts" />
        /// <reference path="tsfiles/ej.web.all.d.ts" />

{% endhighlight %} 

4. Now, initialize the TimePicker component by using ej.TimePicker method. 

{% highlight JS %}

        /// <reference path="tsfiles/jquery.d.ts" />
        /// <reference path="tsfiles/ej.web.all.d.ts" />

        $(function () {
                var sample = new ej.TimePicker($("#timepick"));
            });

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

tsc

{% endhighlight %} 

This command compiles the app.ts file to generate a JS file named app.js file. 
Refer the app.js file in index.html and browse the html file to see the following output.

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
