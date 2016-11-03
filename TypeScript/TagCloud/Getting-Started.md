---
layout: post
title: Getting-Started for TagCloud
description: getting started for TagCloud
platform: Typescript
control: TagCloud
documentation: ug
keywords: TagCloud,js tagcloud,ejtagcloud
---

# Getting Started

This section explains briefly about how to create a **TagCloud** in your application with **Typescript**. The **TagCloud** can be easily configured to the div element in which the tags are placed. The following screenshot illustrates the functionality of a **TagCloud** widget with a list of the topmost search engines. 

![](Getting-Started_images/Getting-Started1.jpg)

## Create TagCloud widget

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
	
Add necessary elements to render TagCloud

{% highlight html %}

    <div id="techWebList"></div>

{% endhighlight %}

Add the following code example to add list of items to the **TagCloud** and initialize the **TagCloud** widget.

{% highlight html %}

      /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
    
     module TagCloudComponent {
     var websiteCollection = [
        { text: "Google", url: "http://www.google.com", frequency: 12 },
        { text: "All Things Digital", url: "http://allthingsd.com/", frequency: 3 },
        { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
        { text: "Business Week", url: "http://www.businessweek.com/", frequency: 2 },
        { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
        { text: "Center Networks", url: "http://www.centernetworks.com/", frequency: 5 },
        { text: "Crave", url: "http://news.cnet.com/crave/", frequency: 8 },
        { text: "Crunch Gear", url: "http://techcrunch.com/gadgets/", frequency: 20 },
        { text: "Daily Tech", url: "http://www.dailytech.com/", frequency: 1 },
        { text: "Electronista", url: "http://www.electronista.com/", frequency: 3 },
        { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
        { text: "Gearlog", url: "http://www.gearlog.com/", frequency: 9 },
        { text: "Information Week", url: "http://www.informationweek.com/", frequency: 0 },
        { text: "PCWorld", url: "http://www.pcworld.com/", frequency: 11 },
        { text: "Tech Republic", url: "http://techrepublic.com/", frequency: 3 },
        { text: "Valleywag", url: "http://valleywag.gawker.com/", frequency: 6 },
        { text: "Rediff", url: "http://in.rediff.com/", frequency: 9 },
        { text: "WebProNews", url: "http://www.webpronews.com/", frequency: 2 }
      ];

     $(function () {
        var sample = new ej.TagCloud($("#techWebList"), {
            titleText: "Popular sites",
            dataSource: websiteCollection,
            fields: {
                text: "text", url: "url", frequency: "frequency"
              }
          });

        });
      }
 
{% endhighlight %}

The following screenshot displays the output of the above code example.

![](Getting-Started_images/Getting-Started1.jpg) 

## Set Min and Max Font Size

In the above code example, the **frequency** properties are used to set the min and max font size to the **TagCloud** list item.

{% highlight javascript %}

     /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
   
     module TagCloudComponent {
        var websiteCollection = [
        { text: "Google", url: "http://www.google.com", frequency: 12 },
        { text: "All Things Digital", url: "http://allthingsd.com/", frequency: 3 },
        { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
        { text: "Business Week", url: "http://www.businessweek.com/", frequency: 2 },
        { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
        { text: "Center Networks", url: "http://www.centernetworks.com/", frequency: 5 },
        { text: "Crave", url: "http://news.cnet.com/crave/", frequency: 8 },
        { text: "Crunch Gear", url: "http://techcrunch.com/gadgets/", frequency: 20 },
        { text: "Daily Tech", url: "http://www.dailytech.com/", frequency: 1 },
        { text: "Electronista", url: "http://www.electronista.com/", frequency: 3 },
        { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
        { text: "Gearlog", url: "http://www.gearlog.com/", frequency: 9 },
        { text: "Information Week", url: "http://www.informationweek.com/", frequency: 0 },
        { text: "PCWorld", url: "http://www.pcworld.com/", frequency: 11 },
        { text: "Tech Republic", url: "http://techrepublic.com/", frequency: 3 },
        { text: "Valleywag", url: "http://valleywag.gawker.com/", frequency: 6 },
        { text: "Rediff", url: "http://in.rediff.com/", frequency: 9 },
        { text: "WebProNews", url: "http://www.webpronews.com/", frequency: 2 }
     ];

      $(function () {
        var sample = new ej.TagCloud($("#techWebList"), {
            titleText: "Popular sites",
            dataSource: websiteCollection,
            fields: {
                text: "text", url: "url", frequency: "frequency"
            }
            });

        });
     }
 
 
{% endhighlight %}

In the above code, the min font size is 0 and max font size is 12.

## Set event to perform an operation

Here, you can set the **TagCloud** events such as create, mouseover, mouseout, click.

{% highlight html %}

     /// <reference path="tsfiles/jquery.d.ts" />
     /// <reference path="tsfiles/ej.web.all.d.ts" />
    
     module TagCloudComponent {

       var websiteCollection = [
        { text: "Google", url: "http://www.google.com", frequency: 12 },
        { text: "All Things Digital", url: "http://allthingsd.com/", frequency: 3 },
        { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
        { text: "Business Week", url: "http://www.businessweek.com/", frequency: 2 },
        { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
        { text: "Center Networks", url: "http://www.centernetworks.com/", frequency: 5 },
        { text: "Crave", url: "http://news.cnet.com/crave/", frequency: 8 },
        { text: "Crunch Gear", url: "http://techcrunch.com/gadgets/", frequency: 20 },
        { text: "Daily Tech", url: "http://www.dailytech.com/", frequency: 1 },
        { text: "Electronista", url: "http://www.electronista.com/", frequency: 3 },
        { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
        { text: "Gearlog", url: "http://www.gearlog.com/", frequency: 9 },
        { text: "Information Week", url: "http://www.informationweek.com/", frequency: 0 },
        { text: "PCWorld", url: "http://www.pcworld.com/", frequency: 11 },
        { text: "Tech Republic", url: "http://techrepublic.com/", frequency: 3 },
        { text: "Valleywag", url: "http://valleywag.gawker.com/", frequency: 6 },
        { text: "Rediff", url: "http://in.rediff.com/", frequency: 9 },
        { text: "WebProNews", url: "http://www.webpronews.com/", frequency: 2 }
    ];

    $(function () {
        var sample = new ej.TagCloud($("#techWebList"), {
            titleText: "Popular sites",
            dataSource: websiteCollection,
			fields: {
                text: "text", url: "url", frequency: "frequency"
              },
            create: function(args) {
                alert();
            },
            mouseover: function (args) {
                alert();
            },
            mouseout: function (args) {
                alert();
            },
            click: function (args) {
                alert();
            },
           
           
         });

       });
   }
 
{% endhighlight %}

In the above code example, the **alert()** function is used  to show the events that happened.

