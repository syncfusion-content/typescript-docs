---
layout: post
title: getting-started
description: getting started
platform: Typescript
control: Splitter
documentation: ug
---

# Getting Started

**Splitter** control consists of movable split bar(s) that divides a container's display area into two or more resizable and collapsible panels. 
From the following guidelines, you can create a Splitter, add Tree view in the Splitter and set actions to view the image. It is used to split the document or image and Expand or Collapse in the Splitter. The following screenshot demonstrates the functionality of Splitter control.

![](getting-started_images\getting-started_img1.png)

## Create a Splitter

Refer the common Typescript [Getting Started Documentation](https://help.syncfusion.com/js/typescript) to create an application and add necessary scripts and styles for rendering the Splitter control.
Create an HTML file and add the scripts references in the order mentioned in the following code example.

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
    <!--Add Splitter here-->
    </body>
    </html>


{% endhighlight %}

Create div element and add in the body tag. To create the Splitter, you should call the `ejSplitter` jQuery plug-in function.


{% highlight html %}

    <div id="outterSpliter">
    </div>

{% endhighlight %}


Initialize the Splitter in app.ts file by using the ej.Splitter method.

{% highlight javascript %}

    /// <reference path="jquery.d.ts" />  
    /// <reference path="ej.web.all.d.ts" />

    module SplitterComponent {
        $(function () {
            let sample = new ej.Splitter($("#outterSpliter"));
        });
    }

{% endhighlight %}


Now build your application, so that the app.js file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file automatically.

## Configure Splitter Panes

Add div element to create Splitter. Save the images in the corresponding location.

{% highlight html %}

    <div class="content-container-fluid">
    <div class="row">
    <div class="cols-sample-area" style="height:400px; margin:0 auto;">
    <div id="outterSpliter">
    <div>					
    <div class="cont">
        <h3 class="h3">Typescript</h3>                          
    </div>
    </div>
    <div>
    <div class="cont">
    <div class="_content">
        Select any product from the tree to show the description.
    </div>
    <div class=" mobile spe" style="display:none">
        <h3>Mobile</h3>
        <img src="galaxy.jpg" />
    </div>
    <div class=" harddisk spe" style="display:none">
        <h3>Harddisk</h3>
        <img src="harddisk.jpg" />
    </div>
    <div class="logo spe" style="display:none">
        <h3>Logo</h3>
        <img src="logo.jpg" />
    </div>
    </div>
    </div>                                     
    </div>
    </div>
    </div>
    </div>
    </div>

{% endhighlight %}

Add the following styles to show the Splitter control in horizontal order.

{% highlight css %}

    .cont {
            padding: 10px 0 0 10px;
            text-align: center;
    }

{% endhighlight %}

## Configure Tree View 

For adding Tree View control, you have to use **ul** element to corresponding element.

Add the following code example in HTML file to configure Tree View.

{% highlight html %}

    <ul id="treeView" class="visibleHide">
        <li> Mobile
                <ul>
                    <li id=" Galaxy " class="_child">Galaxy</li>
                </ul>
        </li>
        <li>Harddisk
                <ul>
                    <li id="Harddisk" class="_child">Segate  </li>
                </ul>
        </li>
        <li>Logo
                <ul>
                    <li id="Logo" class="_child">Amazon</li>
                </ul>
        </li>
    </ul>


{% endhighlight %}

## Set Actions


Add the following code example in the typescript to set the action to view the image. We need to create instance of TreeView to achieve **nodeSelect** event of TreeView.


{% highlight javascript %}

    module SplitterComponent {
        $(function () {
        var splitterInstance = new ej.Splitter($("#outterSpliter"), {
            height: "250px",
            width: "50%",          
            properties: [{paneSize:"50%"}, { }],
            isResponsive:true
        });
    var treeViewInstance = new ej.TreeView($("#treeView"), {
            nodeSelect: (e) => {
                if (e.currentElement.hasClass('e-item last')) {
                    var content = $('.' + e.currentElement[0].id).html();
                    $('._content').html(content);
                }
            },            
            });
    });
    }


{% endhighlight %}

The following screenshot is the output for the above code.

![](getting-started_images\getting-started_img1.png)



> _Note:> You can find the_ Splitter_ properties from the_ [API reference](https://help.syncfusion.com/api/js/ejsplitter) _document_ 

