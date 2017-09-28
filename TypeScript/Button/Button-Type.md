---
layout: post
title: Button-Type
description: button type
platform: TypeScript
control: Button
documentation: ug
---

# Button Type

**Button** is used as normal click able button, submitting form data, resetting the form data to its initial value. According to the usage of button, you can render the button in three types. Using the **type** property, you can easily render the button in following types.

List of Button types

<table>
   <tr>
      <th>Button Types</th>
      <th>Description</th>
   <tr>
      <td>
         button
      </td>
      <td>
         The button is a click able button
      </td>
   </tr>
   <tr>
      <td>
         submit
      </td>
      <td>
         The button is a submit button (submits form-data)
      </td>
   </tr>
   <tr>
      <td>
         reset    
      </td>
      <td>
         The button is a reset button (resets the form-data to its initial values)
      </td>
   </tr>
</table>


The following steps explains you the details about rendering the Button with above mentioned button types.

In the HTML page, add the following button elements to configure Button widget.

{% highlight html %}

<button id="buttonType_button">button</button>
<br />
<br />
<button id="buttonType_submit">submit</button>
<br />
<br />
<button id="buttonType_reset">reset</button>
	
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#buttonType_button"), {
            size: "mini",
            //this type specifies the normal click able button
            type: "button",
            showRoundedCorner: true
        });
       var basicButton1 = new ej.Button($("#buttonType_submit"), {  
            size: "mini",
            //this button is used to submit form data
            type: "submit",
            showRoundedCorner: true
        });
       var basicButton2 = new ej.Button($("#buttonType_reset"), { 
            size: "mini",
            //this button is used to reset the form data to its initial value
            type: "reset",
            showRoundedCorner: true
        });
    });
}
{% endhighlight %}

Execute the above code to render the following output.

![](Button-Type_images/Button-Type_img1.png) 

