---
layout: post
title: Getting-Started
description: getting started
platform: TypeScript
control: WaitingPopup
documentation: ug
keywords: ejwaitingpopup, js waitingpopup, waitingpopup
---

# Getting Started

This section explains briefly about how to create a **WaitingPopup** in your application with **TypeScript**.
**Essential TypeScript WaitingPopup** provides support to display a **WaitingPopup** within your web page. From the following guidelines, you can learn how to create a **WaitingPopup** in a real-time login page authentication scenario. 

The following screenshot illustrates the functionality of a **WaitingPopup** with login page scenario.

![](Getting-Started_images/Getting-Started_img1.png) 

You can give the Username and Password in the **login page**. When you click the **Login** button, you get the **WaitingPopup**. After loading, the alert box pops up with the message “Signed in successfully”.

## Create Username and Password

**Essential TypeScript WaitingPopup** widget basically renders built-in features like blocking the other actions until the page is loaded. You can easily create the **WaitingPopup** widget by using simple **&lt;div&gt;** element as follows.

 Create an HTML file and add the following template to the HTML file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
   <meta charset="utf-8" />
   <title>Getting Started - RichTextEditor</title>
   <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
   <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>  
   <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
</html>

{% endhighlight %}

 Add **&lt;div&gt;** element to render a **WaitingPopup**.

{% highlight html %}

<div id="targetElement">
   <table class="loginTable">
      <tr>
         <td>Username</td>
         <td><input type="text"/></td>
      </tr>
      <tr>
         <td>Password</td>
         <td><input type="password"/></td>
      </tr>
      <tr>
         <td></td>
         <td><button id="target">Login</button></td>
      </tr>
   </table>
   <div id="popup"></div>
</div>

{% endhighlight %}

 Initialize **Click function** using the following code example.

{% highlight js %}
 
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module WaitingpopupComponent {
    $(function () {
 $("#target").click(function () {
            /*Add waiting popup*/
        });
    });

{% endhighlight %}

 Apply the following styles to show the **WaitingPopup**.

{% highlight css %}

<style type="text/css" class="cssStyles">
   #targetElement {
       width: 500px;
       height: 200px;
       margin: 50px;
       border: 1px solid #dbdcdb;
   }
   .loginTable {
       margin: 60px auto;
   }
   #popup_WaitingPopup .e-image {
       display: block;
       height: 70px;
   }
</style>

{% endhighlight %}

The following screenshot displays a **User** **login**.

![](Getting-Started_images/Getting-Started_img2.png) 

## Add WaitingPopup Widget

 In a real-time login page scenario, when you click the Login button, the WaitingPopup is displayed. 

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module WaitingpopupComponent {
    $(function () {
       $("#target").click(function () {
            var waiting = new ej.WaitingPopup($("#popup"), {
                showOnInit: true,
                target: "#targetElement"
            });
            function success() { 
                alert("Signed in successfully");
                waiting.hide();
            }
            setTimeout(success, 5000);
        });
    });
}

{% endhighlight %}

 The following screenshot shows the output of the above code example.

![](Getting-Started_images/Getting-Started_img3.png) 

