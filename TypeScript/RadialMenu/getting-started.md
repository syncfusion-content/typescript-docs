---
layout: post
title: Syncfusion Radial Menu Getting Started
description: getting started
platform: Typescript
control: RadialMenu
documentation: ug
---

# Getting Started

Using the following steps, you can create a Typescript **RadialMenu** control. The basic rendering of Typescript RadialMenu is achieved with default functionality.

![Getting Started](Getting_Started_images\Getting-Started_img1.png)

## Create a RadialMenu

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
    <!--Add RadialMenu here-->
    </body>
    </html>


{% endhighlight %}

Create div element and add in the body tag. To create the RadialMenu, you should call the `ejRadialMenu` jQuery plug-in function.


{% highlight html %}

    <div id="defaultRadialMenu">
        <ul>
            <li data-ej-imageurl="content/images/RadialMenu/font.png" data-ej-text="Bold" data-ej-click="bold"></li>
            <li data-ej-imageurl="content/images/RadialMenu/f1.png" data-ej-text="Italic" data-ej-click="italic"></li>
            <li data-ej-imageurl="content/images/RadialMenu/redo.png" data-ej-text="Redo" data-ej-click="redo" data-ej-enabled="false"></li>
            <li data-ej-imageurl="content/images/RadialMenu/undo.png" data-ej-text="Undo" data-ej-click="undo" data-ej-enabled="false"></li>
        </ul>
    </div>


{% endhighlight %}


Initialize the RadialMenu  in app.ts file by using the ej.RadialMenu method.

{% highlight javascript %}

    /// <reference path="jquery.d.ts" />  
    /// <reference path="ej.web.all.d.ts" />

    module RadialMenuComponent {
    $(function () {
          let sample = new ej.RadialMenu($("#defaultRadialMenu"));
    });
    }

{% endhighlight %}


Now build your application, so that the app.js file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file automatically.

## Image and text configuration

You can set the images for each item by giving the image URL with the **data-ej-imageUrl** attribute in the inner list element and text with **data-ej-text** attribute. Refer to the following code example. 

{% highlight html %}

    <div id="defaultRadialMenu">
        <ul>
            <li data-ej-imageurl="content/images/RadialMenu/font.png" data-ej-text="Bold" ></li>
            <li data-ej-imageurl="content/images/RadialMenu/f1.png" data-ej-text="Italic" ></li>
            <li data-ej-imageurl="content/images/RadialMenu/redo.png" data-ej-text="Redo" data-ej-enabled="false"></li>
            <li data-ej-imageurl="content/images/RadialMenu/undo.png" data-ej-text="Undo" data-ej-enabled="false"></li>
        </ul>
    </div>

{% endhighlight %}

Refer to the following code example to add target content to the **RadialMenu**.

{% highlight html %}

    <div id="radialtarget1" class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <textarea id="rteSample1" rows="10" cols="70" style="height: 440px">
                    <p>
                        Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it.
                        The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart or a diagram.
                        Multiple views of the same data are possible, such as a bar chart for management and a tabular view for accountants.
                        The controller mediates input, converting it to commands for the model or view.The central ideas behind MVC are code reusable and in addition to dividing the application into three kinds of components, the MVC design defines the interactions between them.
                    </p>

                    <p>A controller can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). It can also send commands to the model to update the model's state (e.g., editing a document).</p>

                    <p>A model notifies its associated views and controllers when there has been a change in its state. This notification allows the views to produce updated output, and the controllers to change the available set of commands. A passive implementation of MVC omits these notifications, because the application does not require them or the software platform does not support them.</p>

                    <p>A view requests from the model the information that it needs to generate an output representation to the user.</p>
                </textarea>
            </div>
        </div>
    </div>


{% endhighlight %}

Add the following styles in your code.

{% highlight css %}

    .e-radialmenu .imageClass {
                background-image: url(content/images/RadialMenu/settings.png);
            }

    .e-radialmenu .backImageClass {
                background-image: url(content/images/RadialMenu/Back_button.png);
            }

    textarea {
                padding: 10px;
            }
    #defaultRadialMenu {
                pointer-events:none;
            }
    .e-radial,#defaultradialmenu_svgdiv {
                pointer-events:all;
            }

{% endhighlight %}

## Displaying RadialMenu

You can display the Radial Menu by performing desired action on the target content while selecting the text inside the target. Therefore, call the **select** event of RTE the content. Refer to the following code example and add it to the script.

{% highlight javascript %}

    declare var rteObj: any;
    declare var data: any;
    var radialElement = $('#defaultRadialMenu'), action = 0, forRedo = 0;
    var rteElement = $("#rteSample1");
    module RadialMenuComponent {
    $(function () {

    if (!(ej.browserInfo().name == "msie" && parseInt(ej.browserInfo().version) < 9)) {
        var radialMenuInstance = new ej.RadialMenu($("#defaultRadialMenu"), {
            imageClass: "imageClass",
            backImageClass: "backImageClass",
            targetElementId: "radialtarget1"
        });
    $("#radialtarget1").parent().css("position", "relative");
    }
    var rteInstance = new ej.RTE($("#rteSample1"), {
        width: "100%",
        minWidth: "10px",
        change: (e) => { radialElement.ejRadialMenu("enableItem", "Undo"); },
        select: (e) => {
            var target = $("#radialtarget1"), radialRadius = 150, radialDiameter = 2 * radialRadius,
                // To get Iframe positions
                iframeY = e.event.clientY, iframeX = e.event.clientX,
                // To set Radial Menu position within target
                x = iframeX > target.width() - radialRadius ? target.width() - radialDiameter : (iframeX > radialRadius ? iframeX - radialRadius : 0),
                y = iframeY > target.height() - radialRadius ? target.height() - radialDiameter : (iframeY > radialRadius ? iframeY - radialRadius : 0);
            radialElement.ejRadialMenu("setPosition", x, y);
            radialElement.focus();
            $('iframe').contents().find('body').blur();
        },
        showToolbar: false,
        showContextMenu: false
    });
    });
    }

{% endhighlight %}

Run the above code and select any text inside the target. The settings icon is displayed. Click that icon to render the following output.

![Displaying Radial Menu](Getting_Started_images\getting-started_img2.png)


## RadialMenu item functionalities


You can set the functionalities for each item and define click function by using **data-ej-click** attribute. Refer to the following code example. Define the click function for Radial Menu control items as follows.


{% highlight html %}

    <div id="defaultRadialMenu">
        <ul>
            <li data-ej-imageurl="content/images/RadialMenu/font.png" data-ej-text="Bold" data-ej-click="bold"></li>
            <li data-ej-imageurl="content/images/RadialMenu/f1.png" data-ej-text="Italic" data-ej-click="italic"></li>
            <li data-ej-imageurl="content/images/RadialMenu/redo.png" data-ej-text="Redo" data-ej-click="redo" data-ej-enabled="false"></li>
            <li data-ej-imageurl="content/images/RadialMenu/undo.png" data-ej-text="Undo" data-ej-click="undo" data-ej-enabled="false"></li>
        </ul>
    </div>

{% endhighlight %}

Refer to the following code example to add functionalities for each items in **click** event and you can enable items in RadialMenu by using **change** event in typescript file.

{% highlight javascript %}

    function bold(e: any) {

    rteObj = rteElement.data("ejRTE");
    rteObj.executeCommand("bold");
    data = rteObj._getSelectedHtmlString() ? true : false;
    if (data) action += 1;
    forRedo = action;
    radialElement.focus();
    }
    function italic(e: any) {
    rteObj = rteElement.data("ejRTE");
    rteObj.executeCommand("italic");
    data = rteObj._getSelectedHtmlString() ? true : false;
    if (data) action += 1;
    forRedo = action;
    radialElement.focus();
    }
    function undo(e: any) {
    rteObj = rteElement.data("ejRTE");
    rteObj.executeCommand("undo");
    action -= 1;
    if (action == 0)
        radialElement.ejRadialMenu("disableItem", "Undo");
    radialElement.ejRadialMenu("enableItem", "Redo");
    radialElement.focus();
    }
    function redo(e: any) {
    rteObj = rteElement.data("ejRTE");
    rteObj.executeCommand("redo");
    action += 1;
    if (forRedo == action) radialElement.ejRadialMenu("disableItem", "Redo");
    radialElement.ejRadialMenu("enableItem", "Undo");
    radialElement.focus();
    }

{% endhighlight %}

Run the above code and select any text inside the target. The settings icon is displayed. Click that icon to render the RadialMenu control. Click **bold** item in RadialMenu control, to render the following output.


![Radial Menu items functionalities](Getting_Started_images\Getting_Started_img3.png)


> _Note:> You can find the_ RadialMenu _properties from the_ [API reference](https://help.syncfusion.com/api/js/ejradialmenu) _document_ 

