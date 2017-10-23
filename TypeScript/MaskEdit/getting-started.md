---
layout: post
title: getting-started
description: getting started
platform: Typescript
control: MaskEdit
documentation: ug
---

# Getting Started



Using the following steps, you can create a **Typescript** MaskEdit component.

## Creating an MaskEdit in TypeScript



You can create a **Typescript** application with the help of the given [Typescript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

 Within an index.html file and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<title>TypeScript Application</title>
<link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
<script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>

</head>
<body>
<!--Add MaskEdit sample  here-->
</body>
</html>


{% endhighlight %}



The  can be created from a `input` element with the HTML `id` attribute and pre-defined options set to it.



{% highlight html %}

<input id="maskEdit" type="text" />
<script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
    var mask = new ej.MaskEdit($("#maskEdit"), {
            name: "mask",
            value: "4242422424",
            maskFormat: "99 999-99999",
            width: "100%"
        })
}

{% endhighlight %}



* Now build your application, so that the **app.ts** file will compiled and automatically generated the **app.js** file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file by compiling     build the application.



Execution of above code will render the following output.

![](getting-started_images/getting-started_img1.png)


## Error Visibility

* The MaskEdit has an option that shows the error value with red colored text. It is used to validate the Mask Edit value. You can set the showError property as “true” to enable this option.


{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module EditorComponent {
  var mask = new ej.MaskEdit($("#maskEdit"), {
            name: "mask",
            value: "123456",
            maskFormat: "99 999-99999",
            width: "100%",
            showError: true
        })
}
{% endhighlight %}


* Execution of above code will render the following output

![](getting-started_images/getting-started_img2.png)


## CustomCharacter

The MaskEdit allows you to use the custom character option. The specified character is only allowed to enter in the Mask Edit Textbox by using the customCharacter property.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

var mask = new ej.MaskEdit($("#maskEdit"), {
    name: "mask",
    value: "4242424",
    maskFormat: "9C 9C9-9C",
    width: "100%",
    customCharacter: "$"
})
{% endhighlight %}
