---
layout: post
title: Syncfusion Radial Menu Template Support
description: Template Support.
platform: Typescript
control: RadialMenu
documentation: ug
---

## Template Support

 Template support for RadialMenu items will allow you to use any type of [\<svg\>](https://developer.mozilla.org/en-US/docs/Web/SVG/Element#SVG_elements) permitted tags inside our template. Here for example, using this template support you can use the SVG icons in Radial Menu instead of image tags. To use SVG icons in RadialMenu, you need to use [prependTo](https://help.syncfusion.com/api/js/ejradialmenu#members:items-prependTo) property.

 ### Add SVG to item Icon

Using SVG icon will optimize the icons quality and to reduce space occupation by normal images and svg images are scalable and zoom. Define the text element for SVG with x and y position and code for rendering the font icons. Assign the SVG element ID to **prependTo** property.

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
        <div id="defaultRadialMenu">
        <ul>
            <li data-ej-prependTo="#template1" data-ej-text="Bold" data-ej-click="bold"></li>
            <li data-ej-prependTo="#template2" data-ej-text="Italic" data-ej-click="italic"></li>
            <li data-ej-prependTo="#template3" data-ej-text="Redo" data-ej-click="redo" data-ej-enabled="false"></li>
            <li data-ej-prependTo="#template4" data-ej-text="Undo" data-ej-click="undo" data-ej-enabled="false"></li>
        </ul>
    </div>

     <svg id="template1" style="display: none" xmlns="http://www.w3.org/2000/svg">
        <text x="210" y="100">&#xe636;</text>
    </svg>
    <svg id="template2" style="display: none" xmlns="http://www.w3.org/2000/svg">
        <text x="210" y="218">&#xe635;</text>
    </svg>
    <svg id="template3" style="display: none" xmlns="http://www.w3.org/2000/svg">
        <text x="90" y="215">&#xe606;</text>
    </svg>
    <svg id="template4" style="display: none" xmlns="http://www.w3.org/2000/svg">
        <text x="93" y="100">&#xe607;</text>
    </svg>
    
{% endhighlight %}

Now add the following in your Script section,

{% highlight javascript %}

    <script type="text/javascript">
        var rteObj, rteElement = $("#rteSample1"), radialElement = $('#defaultRadialMenu'), action = 0, forRedo = 0;
        $(function () {
            rteElement.ejRTE({ width: "100%", minWidth: "10px", change: "rteChange", select: "radialShow", showToolbar: false, showContextMenu: false });
            rteObj = rteElement.data("ejRTE");
            if (!(ej.browserInfo().name == 'msie' && ej.browserInfo().version < 9)) {
                radialElement.ejRadialMenu({ imageClass: "imageClass", backImageClass: "backImageClass", targetElementId: "radialtarget1" });
				$("#radialtarget1").parent().css("position", "relative");
            }
            else {
                $("#contentDiv").html("Radial Menu is only supported from Internet Explorer Versioned 9 and above.").css({ "font-size": "20px", "color": "red" });
            }
			$(window).resize(function(){
				if(ej.isMobile() && ej.isPortrait())
					$('#defaultRadialMenu').css({"left":25})
			});
        });
        function radialShow(e) {
            var target = $("#radialtarget1"), radialRadius = 150, radialDiameter = 2 * radialRadius,
                // To get Iframe positions
                iframeY = e.event.clientY, iframeX = e.event.clientX,
                // To set Radial Menu position within target
                x = iframeX > target.width() - radialRadius ? target.width() - radialDiameter : (iframeX > radialRadius ? iframeX - radialRadius : 0),
                y = iframeY > target.height() - radialRadius ? target.height() - radialDiameter : (iframeY > radialRadius ? iframeY - radialRadius : 0);
            radialElement.ejRadialMenu("setPosition", x, y);
            radialElement.focus();
			$('iframe').contents().find('body').blur();
        }
        function rteChange(e) {
            radialElement.ejRadialMenu("enableItem", "Undo");
        }
        function bold(e) {
            rteObj.executeCommand("bold");
            data = rteObj._getSelectedHtmlString() ? true : false;
            if (data) action += 1;
            forRedo = action;
            radialElement.focus();
        }
        function italic(e) {
            rteObj.executeCommand("italic");
            data = rteObj._getSelectedHtmlString() ? true : false;
            if (data) action += 1;
            forRedo = action;
            radialElement.focus();
        }
        function undo(e) {
            rteObj.executeCommand("undo");
            action -= 1;
            if (action == 0)
                radialElement.ejRadialMenu("disableItem", "Undo");
            radialElement.ejRadialMenu("enableItem", "Redo");
            radialElement.focus();
        }
        function redo(e) {
            rteObj.executeCommand("redo");
            action += 1;
            if (forRedo == action) radialElement.ejRadialMenu("disableItem", "Redo");
            radialElement.ejRadialMenu("enableItem", "Undo");
            radialElement.focus();
        }
    </script>

{% endhighlight %}

Add the following in style section,

{% highlight css %}

    <style>
         .e-radialmenu .imageClass {
            background-image: url(../content/images/RadialMenu/settings.png);
        }
        @font-face {
            font-family: 'ej-webfont';
            src: url('../content/ejthemes/common-images/icons.eot');
            src: url('../content/ejthemes/common-images/icons.ttf') format('truetype'),
                 url('../content/ejthemes/common-images/icons.woff') format('woff'),
                 url('../content/ejthemes/common-images/icons.svg') format('svg');
            font-weight: normal;
            font-style: normal;
            font-size: 20px;
        }

        .e-radialmenu .e-abs.e-radialshow, .e-radialmenu .e-abs.e-scaleshow {
            /* use !important to prevent issues with browser extensions that change fonts */
            font-family: 'ej-webfont' !important;
            speak: none;
            font-size: 20px;
            font-style: normal;
            font-weight: normal;
            font-variant: normal;
            text-transform: none;
            line-height: 1;
            -webkit-font-smoothing: antialiased;
            /* Better Font Rendering =========== */
            -webkit-font-smoothing: antialiased;
        }

        .e-bold:before {
            content: "\e636";
        }

        .e-italic:before {
            content: "\e635";
        }

       .e-icon.e-redo:before {
            content: "\e606"; 
        }

        .e-icon.e-undo:before {
            content: "\e607";
        }
    </style>

{% endhighlight %}

The following screenshot illustrates the output,

![Template support](template-support\img1.png)

     N> This is the example sample for SVG icon support for Radial Menu.Like wise you can add any SVG element to it, but you need to customize and position the element individually.  


