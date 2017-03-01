---
layout: post
title: getting started
description: getting started
platform: Typescript
control: Signature
documentation: ug
---

# Getting Started

Using the following steps, you can create a **Typescript** Signature component. The basic rendering of **Typescript** Signature is achieved with default functionality.

## Creating an Signature in Typescript

You can create a **Typescript** application with the help of the given [Typescript Getting Started Documentation.](https://help.syncfusion.com/js/typescript)

Within an index.html file and add the scripts references in the order mentioned in the following code example.

{% highlight html %}
    <!DOCTYPE html>
    <html>
    <head>
        <title>Typescript Application</title>
        <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
        <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    </head>
    <body>
        <!--Add Signature here-->
    </body>
    </html>

{% endhighlight %}


The Signature can be created from a HTML ‘input’ element with the HTML ‘id’ attribute and pre-defined options set to it. To create the Signature, you should call the ejSignature jQuery plug-in function.

{% highlight html %}

<div style="width:300px;height:600px;">

<div id="signature" />

 </div>


{% endhighlight %}


Create app.ts file and past the below content

{% highlight js %}

            /// <reference path="jquery.d.ts" />
            /// <reference path="ej.web.all.d.ts" />

            module SignatureComponent { 
                $(function () { 
                    var basicSignature = new ej.Signature($("#signature"), {
                    });
                }
{% endhighlight %}


Now build your application, so that the **app.js** file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file automatically.

This will render a Signature like below.

![https://help.syncfusion.com/js/signature/Getting_Started_images/createsignaturecontrol_img1.png](Getting_Started_images\creatingansignatureintypescript_img1.png)


## Adjusting Signature Size

You can customize the width and height of the Signature by **width** and **height** properties. These properties completely depend on signature canvas. The width and height are adjusted within the signature canvas.

The following code example is used to render the Signature component with customized width and height.

{% highlight js %}

<div id="signature" /> 
<script src="app.js"></script>

{% endhighlight %}


{% highlight js %}


            /// <reference path="jquery.d.ts" />
            /// <reference path="ej.web.all.d.ts" />
            module SignatureComponent { 
                $(function () { 
                    var basicSignature = new ej.Signature($("#signature"), {
                        height: "300px",
                        width:”200px”,
                        isResponsive:true
                });
            }


{% endhighlight %}


The following screenshot illustrates signature with customized width and height.

![https://help.syncfusion.com/js/signature/Getting_Started_images/adjustingsignaturesize_img1.png](Getting_Started_images\adjustingsignaturesize_img1.png)



