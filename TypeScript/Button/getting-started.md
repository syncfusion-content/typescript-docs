---
layout: post
title: create a simple button in typescript
description: create a simple button in typescript
platform: js
control: Overview
documentation: ug
---

## Create a simple Button in Typescript

You can create a **Typescript** application with the help of the given [Typescript Getting Started Documentation](https://help.syncfusion.com/js/typescript).

Create an **HTML** page and add the scripts references in the order, mentioned in the above link Create the **Button** control as follows.



<body>
<table>
    <tr>
        <td >My First Button</td>
        <td>
            <input id="button" value="button"/>
        </td>
    </tr>
</table> 
</body>





/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var sample = new ej.Button($("#button"));
    });
}

## Configuring Button Properties



This section encompasses the details on how you can configure the Button control in your application and customize it with various properties such as various size, resizing the**Button** according to your requirement.

To render the button with required text, size and with rounded corner add the following code example in your TS file.



/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var sample = new ej.Button($("#button"), { text: "Button", showRoundedCorner: true });
    });
}




The following screenshot illustrates the **Button** control with text, size and rounded corner properties.



![](getting-started_images/getting-started_img1.png)

