---
layout: post
title: Getting-Started | ColorPicker | TypeScript | Syncfusion
description: Getting Started
platform: TypeScript
control: ColorPicker
documentation: ug
---

# Getting Started


Using the following steps, you can create a **TypeScript** ColorPicker component.

## Creating an ColorPicker in TypeScript


You can create a **TypeScript** application with the help of the given [TypeScript Getting Started Documentation](https://help.syncfusion.com/js/typescript).


To create a ColorPicker, add a `input` element with the HTML `id` attribute and pre-defined options set to it.


{% highlight html %}

        <input id="ColorPicker" type="text" />
        <script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

        /// <reference path="jquery.d.ts" />  
        /// <reference path="ej.web.all.d.ts" />

        module ColorPickerComponent {
            var colorPickObj = new ej.ColorPicker($("#ColorPicker"), {
                    value: "#278787"
                })
        }

{% endhighlight %}


* Now build your application, so that the **app.ts** file will compiled and automatically generated the **app.js** file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file by compiling     build the application.


Execution of above code will render the following output.

![Creating an ColorPicker in TypeScript](getting-started_images/getting-started_img1.png)

