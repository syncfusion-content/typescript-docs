---
layout: post
title: Getting started for Tooltip
description: How to create the Tooltip in Typescript
platform: Typescript
control: Tooltip
documentation: ug
keywords : ejTooltip, Tooltip, js Tooltip, Tooltip widget
---
# Getting started

## Preparing HTML document

The Tooltip control has the following list of external JavaScript dependencies. 

* [jQuery](http://jquery.com/) 1.7.1 and later versions

* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing/) - to support animation effects in the components

Refer to the internal dependencies in the following table.

<table>
<tr>
<th>
File                                </th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js</td><td>
It is referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.tooltip.min.js</td><td>
The Tooltip's main file.</td></tr>
</table>

To get started, you can use the `ej.web.all.min.js` file that encapsulates all the `ej` controls and frameworks in one single file.

## Create a Tooltip

Create an **HTML** page and add the scripts references in the order mentioned in the following code example.

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
	
The Tooltip can be created from any HTML element with the HTML `id` attribute and pre-defined options set to it. To create the Tooltip, you should call the `ejTooltip` jQuery plug-in function with the options as parameter. Refer to the following code example.

{% highlight html %}
 
      <div class="frame">
      <div class="img"  id="link1"  >
        <img src="http://js.syncfusion.com/demos/web/images/tooltip/template-05.png" alt="Delphi">
        <div class="desc">Delphi Succinctly</div>
     </div>
     </div>

{% endhighlight %}

{% highlight html %}
   
    /// <reference path="../tsfiles/jquery.d.ts" />
    /// <reference path="../tsfiles/ej.web.all.d.ts" />

    module TooltipComponent {
    
     $(function () {

        var sample1 = new ej.Tooltip($("#link1"),{
            content: "Learn the fundamentals of Delphi to build a variety of solutions for many devices and platforms." });

            });
       }

{% endhighlight %}

Apply the following style sheet

{% highlight html %}

    <style>
       div.img {
        border: 1px solid #ccc;
        width: 159px;
        height: 213px;
        left: 35%;
        position: relative;
        top: 20%;
      }
     div.img img {
        width: 159px;
        height: 179px;
       }
     div.desc {
        padding: 8px;
        text-align: center;
       }
    </style>
    
{% endhighlight %}

![](Getteing-Started_images/Getteing-Started_img1.jpeg)

## Setting Dimensions

Tooltip dimensions can be set using [width](http://help.syncfusion.com/js/api/ejtooltip#members:width) and [height](http://help.syncfusion.com/js/api/ejtooltip#members:height) API.

{% highlight html %}
 
     /// <reference path="../tsfiles/jquery.d.ts" />
     /// <reference path="../tsfiles/ej.web.all.d.ts" />

        module TooltipComponent {
    
             $(function () {

            var sample1 = new ej.Tooltip($("#link1"),{
            content: "Learn the fundamentals of Delphi to build a variety of solutions for many devices and platforms.",
            height:"100px",
			width:"100px"			
			});

         });
       }

{% endhighlight %}


## Tooltip Appearance 

You can configure the appearance of the Tooltip with the title, close button and call out as your application requires.

{% highlight html %}
 
      /// <reference path="../tsfiles/jquery.d.ts" />
     /// <reference path="../tsfiles/ej.web.all.d.ts" />

     module TooltipComponent {
    
        $(function () {

          var sample1 = new ej.Tooltip($("#link1"),{
             content: "Learn the fundamentals of Delphi to build a variety of solutions for many devices and platforms.",
             height:"100px",
			 width:"200px",
             closeMode:"sticky",
             title:"Delphi Succintly",
             isBalloon : false 
			});

            });
        }    
{% endhighlight %}

Apply the following styles to show the Tooltip.

{% highlight html %}

    <style>
       div.img {
        border: 1px solid #ccc;
        float: left;
        box-sizing: border-box;
        height: 200px;
        width: 146px;
         }
        div.img img{
        width: 100%;
        height: 166px;
        }
       div.desc {
        padding: 6px;
        text-align: center;
         }
    </style>
    
{% endhighlight %}

![](Getteing-Started_images/Getteing-Started_img2.jpeg)

