---
layout: post
title: getting started
description: getting started
platform: typescript
control: DateRangePicker
documentation: ug
---

# Getting Started

This section explains you how to render and configure DateRangePicker component in a TypeScript application.


## Create your first DateRangePicker	

1. Create a TypeScript application and refer the dependent modules, script and CSS with the help of given Getting started document.

2. In the index.HTML file, add the input element for rendering DateRangePicker component as given below.

{% highlight html %}

        <input id="daterangepick" />

{% endhighlight %} 

3. Create a TypeScript file named "app.ts" file and refer the required definition files as given below.

{% highlight JS %}

        /// <reference path="tsfiles/jquery.d.ts" />
        /// <reference path="tsfiles/ej.web.all.d.ts" />

{% endhighlight %} 

4. Now, initialize the DateRangePicker component by using ej.DateRangePicker method. 

{% highlight JS %}

        /// <reference path="tsfiles/jquery.d.ts" />
        /// <reference path="tsfiles/ej.web.all.d.ts" />

        $(function () {
                var sample = new ej.DateRangePicker($("#daterangepick"));
            });

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

tsc

{% endhighlight %} 

This command compiles the app.ts file to generate a JS file named app.js file. 
Refer the app.js file in index.html and browse the html file.

## Get/Set Value

DateRangePicker provides an options to configure all its properties and to get its value. DateRangePicker value can be assigned during initialization or at run time. Below code shows how to assign the values at initialization.

{% highlight js %}

     // initialize DateRangePicker component with Value API

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var sample = new ej.DateRangePicker($("#daterangepick"), {

                value: "11/1/2013 - 12/3/2019", // sets the date range
            });
       });
}

{% endhighlight %}






