---
layout: post
title: Getting Started with TypeScript ProgressBar Control | Syncfusion
description: Learn here all about Getting Started in Syncfusion Essential TypeScript ProgressBar control, its elements, and more.
platform: TypeScript
control: ProgressBar
documentation: ug
keywords: ejprogressbar, js progressbar, progressbar
---

# Getting Started with TypeScript ProgressBar

This section briefly describes how to create a **ProgressBar** control using **TypeScript** and learn its features.
**Essential TypeScript** **ProgressBar** displays a **ProgressBar** within a web page that allows you to show the progress of an event. Here, you can learn how to customize the progress and color of the **ProgressBar** in a real-time application to indicate the strength of the password, where the progress changes with respect to the change in length of the password. This helps you to validate the password is typed. 

The following screenshot shows the **ProgressBar.**


![Getting Started with TypeScript ProgressBar](Getting-Started_images/Getting-Started_img1.png) 

## Create a ProgressBar

**Essential TypeScript ProgressBar** widget is created using a simple **&lt;div&gt;** element. This element provides built-in features that allow you to change the progress, size and text of the control.

You can create the **ProgressBar** widget by using a simple input **&lt;div&gt;** element as follows:

 Create an **HTML** file and add the following template to the **HTML** file to create your ProgressBar. It also includes the necessary scripts and styles.

{% highlight html %}

<!doctype html>
<html>
    <head>
    <meta charset="utf-8" />
    <title>Getting Started - RichTextEditor</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>  
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    </head>
   <body>
      <! -- add rating element here -->
   </body>
</html>

{% endhighlight %}

 Add **&lt;input&gt;** element inside the **&lt;body&gt;** tag of your file to create a **ProgressBar.**

{% highlight html %}

<div style="content-container-fluid">
   <div class="row">
      <div class="cols-sample-area">
         <div class="frame">
            <div class="wrap_up">
               <!--Initializing password field*-->
               <label for="startButton">Password</label>
               <input type="password" id="password" style="border-radius:0px"/>
            </div>
            <div class="control">
               <!--initializing ProgressBar control-->
               <div id="progressBar"></div>
            </div>
         </div>
      </div>
   </div>
</div>

{% endhighlight %}

It also includes a Password field and through that the progress of the **ProgressBar** can be controlled
 
Initialize the ProgressBar in ts file by using the `ej.ProgressBar` method.

{% highlight javascript %}
    
/// <reference path="jquery.d.ts" />  
/// <reference path="scripts/typings/ej/ej.web.all.d.ts" />
      
module ProgressBarComponent {
    $(function () {
         var progress = new ej.ProgressBar($("#progressBar"), {
            height: 20,
            value: 30,  /*Specify the initial value of the progress in percentage*/
            width: 200,

        });
        progress.option("text", "weak");
        $(".e-progress").css({ "background-color": "#DE0909", "border-radius": "10px" });
        $(".e-progressbar").css({ "border-radius": "10px", "border": "1px solid black" });
    });
}

{% endhighlight %}

Here, you can initialize the properties of the **ProgressBar** such as height, value, width, text that is applied to the control by default.

The following screenshot displays a **ProgressBar** control.

![Create ProgressBar in TypeScript](Getting-Started_images/Getting-Started_img2.png) 

Include the following code within the **&lt;head&gt;** tag to change the page layout.

{% highlight css %}

<style type="text/css" class="cssStyles">
   /*applying styles */
   .frame {
       border: 1px solid #BBBCBB;
       border-radius: 10px 10px 10px 10px;
       padding: 50px 60px;
       margin-top: 40px;
       width: 400px;
       margin-left: 400px;
   }
   .control {
       margin-bottom: 5px;
       margin-left: 230px;
   }
   .wrap_up {
       margin-left: 105px;
       font-size: 18px;
   }
   #progressBar {
       margin-top: 10px;
   }
</style>

{% endhighlight %}

## Progress Control using Length of the Password Field

In real-time scenario, the progress of **ProgressBar** is changed according to the length of text in the password field by binding the change in the properties of control and checking the length of the password field.

Add the following code example inside the **&lt;script&gt;** tag of your **HTML** file.

{% highlight javascript %}

/// <reference path="jquery.d.ts" />  
/// <reference path="scripts/typings/ej/ej.web.all.d.ts" />
      
module ProgressBarComponent {
    var progresObj, buttonObj, k = 10, timer = window.clearInterval(timer), i = 0, obj;
    $(function () {
         var progresObj = new ej.ProgressBar($("#progressBar"), {
            height: 20,
            value: 30,  /*Specify the initial value of the progress in percentage*/
            width: 200,

        });
        progresObj.option("text", "weak");
        $(".e-progress").css({ "background-color": "#DE0909", "border-radius": "10px" });
        $(".e-progressbar").css({ "border-radius": "10px", "border": "1px solid black" });
    });
$(document).keypress(function () {    //To capture the keypress inside the document           
    i = $("#password").val().length;
    if (i < 5)
       weak();
    else if (i == 5 || i < 7)
       Strong();
    else if (i == 7 || i > 7)
    very_strong();
});
function Strong() {     //Change the width and text of the progress ... called when the length is greater than 5
    progresObj.option("text", "strong");
    progresObj.option("percentage", k + 50);
    $(".e-progress").css("background-color", "#0055FF");
    $(".e-progressbar").css("color", "#000000");
}
function very_strong() {     //Change the width and text of the progress ... called when the length is greater than 7
    progresObj.option("text", "Very strong");
    progresObj.option("percentage", k + 90);
    $(".e-progress").css("background-color", "Green");
    $(".e-progressbar").css("color", "#000000");
}
function weak() {     //Change the width and text of the progress... called when the length is less than 5
    progresObj.option("text", "Weak");
    progresObj.option("percentage", k + 20);
    $(".e-progress").css("background-color", "#DE0909");
    $(".e-progressbar").css("border-radius", "10px");
}
}

{% endhighlight %}

You can calculate length of the password and call the appropriate function that changes the percentage property of **ProgressBar**.

* The **weak()** function changes the text inside the ProgressBar to **Weak** and percentage to 30, that is invoked when the length of the text is less than 5.
* The **strong()** function changes the text inside the ProgressBar to **Strong** and percentage to 60, that is invoked when the length of the text exceeds 5.
* The **very_strong()** function changes the text inside the ProgressBar to Very **Strong** and percentage to 100, that is invoked when the length of the text exceeds 7 and the text contains a symbol in it.

You can change themes or appearance of the ProgressBar as required.

The final output is displayed as follows.

![Start Properties in TypeScript ProgressBar](Getting-Started_images/Getting-Started_img3.png) 

![Complete Properties in TypeScript ProgressBar](Getting-Started_images/Getting-Started_img4.png) 

![Change Properties in TypeScript ProgressBar](Getting-Started_images/Getting-Started_img5.png) 

You can also bind an event at the start and finish of a ProgressBar by using the start, complete and change properties of the ProgressBar.

