---
layout: post
title: create a simple SplitButton in TypeScript
description: create a simple SplitButton in TypeScript
platform: TypeScript
control: Overview
documentation: ug
---

## Create a simple SplitButton in TypeScript

You can create a **TypeScript** application with the help of the given [getting started documentation](https://help.syncfusion.com/js/typescript).

* Create an **HTML** page and add the scripts references in the order, mentioned in the above link to create the **SplitButton** control as follows.

{% highlight html %}

    <body>
        <button id="splitbuttonnormal"></button>
        <ul id="menu1">
            <li><span>User</span></li>
            <li><span>Guest</span></li>
            <li><span>Admin</span></li>
        </ul>
    </body>   

{% endhighlight %}

* Create app.ts file and use the below content

{% highlight javascript %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module ButtonComponent {
        $(function () {
            var splitbuttonnormal = new ej.SplitButton($("#splitbuttonnormal"), {
                targetID: "menu1"
            });
        });
    }    

{% endhighlight %}

You can execute the above code example to display the **SplitButton** control.

![](getting-started_images/getting-started_img2.png) 

## Configuring SplitButton Properties

This section encompasses the details on how you can configure the SplitButton control in your application and customize it with various properties such as various size, resizing the **SplitButton** according to your requirement.

To render the SplitButton with required text, size and rounded corner add the following code example in your TS file.

{% highlight javascript %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module ButtonComponent {
        $(function () {
            var splitbuttonnormal = new ej.SplitButton($("#splitbuttonnormal"), {
                showRoundedCorner: true,
                size: "large",
                prefixIcon: "e-icon e-key",
                targetID: "menu1",
                contentType: "textandimage",
                text: "login"
            });
        });
    }  
   
{% endhighlight %}

The following screenshot illustrates the **Split Button** control with text, size and rounded corner properties.

![](getting-started_images/getting-started_img1.png) 


