---
layout: post
title: Getting-Started
description: Getting Started
platform: typescript
control: dialog
documentation: ug
---

# Getting Started

This section helps you to understand the getting started of the Dialog control with the step-by-step instructions.

# Create a Dialog

The following steps guide you to add a Dialog control.

1)	Refer the common Typescript [Getting Started Documentation](https://help.syncfusion.com/js/typescript) to create an application and add necessary scripts and styles for rendering the Dialog control.

2)  Create an HTML page and add the scripts and css references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Typescript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>
<body>
    <!--Add Dialog code here-->
</body>
</html>

{% endhighlight %}

3)	Add the following code with in the <body> tag to render the Dialog control. 

{% highlight html %}

      <div id="basicDialog">

      </div>

{% endhighlight %}

Initialize the Dialog control in ts file by using the ej.Dialog method.

{% highlight ts %}

/// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module DialogComponent {
    $(function () {
        var dialogInstance = new ej.Dialog($("#basicDialog"), {
            
        });
    });
}

{% endhighlight %}

To get the following output from the above-mentioned code.

![](getting-started-images/getting-started-img1.png)

## Add dialog content

Add the below code to render dialog control with content.

{% highlight html %}

       <div id="basicDialog">
            <p>This is a simple dialog</p>
       </div>
       
{% endhighlight %}

To get the following output from the above-mentioned code

![](getting-started-images/getting-started-img2.png)

## Set the title

To set the dialog control title as using the below mentioned code.

{% highlight html %}

       <div id="basicDialog" title="Dialog">
            <p>This is a simple dialog</p>
       </div>

{% endhighlight %}

To get the following output from the above-mentioned code.

![](getting-started-images/getting-started-img3.png)

## Open Dialog dynamically

In most cases, the Dialog controls are needed only in dynamic actions like showing some messages on clicking a button, to provide alert, etc. So, the Dialog control provides “open” and “close” methods to open/close the dialogs dynamically.
The Dialog control can be hidden on initialize using showOnInit property which should be set to false.
The dialog will be opened on clicking the Button control. Refer to the below mentioned code.

{% highlight html %}

<input class="e-btn" id="btnOpen" value="Click to open dialog" />
    <div class="control">
        <div id="basicDialog" title="Dialog">
            <p>This is a simple dialog</p>

            </div>
        </div>
    </div>

{% endhighlight %}

{% highlight ts %}

module DialogComponent {
    $(function () {
        var dialogInstance = new ej.Dialog($("#basicDialog"), {
			target:".control",
            showOnInit: false,
            close:()=>{
			$("#btnOpen").show();}
        });
        var btnInstance = new ej.Button($("#btnOpen"), {
            size: "medium",
            click: ()=>{
			$("#btnOpen").hide();
            $("#basicDialog").ejDialog("open");},
            type: "button",
            
        });
    });
}

{% endhighlight %}

To get the following output from the above-mentioned code.

![](getting-started-images/getting-started-img4.png)


N> You can find the Dialog control properties from the [API reference](https://help.syncfusion.com/api/js/ejdialog).             
