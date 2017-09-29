---
layout: post
title: Custom Buttons
description: Custom Buttons
platform: TypeScript
control: Button
documentation: ug
---
# Custom Buttons

Essential JavaScript Button control has an option of using normal ejButton as **Custom Button** to give visual weight to ejButton which helps user interface to notify and differentiate the priority action button with the other normal buttons.

Custom Buttons includes six predefined button styles and each button indicates unique sign of action to the user.

List of Custom Buttons

<table>
   <tr>
      <th>Button Types</th>
      <th>Class</th>
      <th>Description</th>
   <tr>
      <td>Primary Button</td>
      <td>e-primary</td>
      <td>Provides extra visual weight and identifies the primary action in a set of buttons</td>
  </tr>
   <tr>
      <td>Link Button</td>
      <td>e-link</td>
      <td>Deemphasize a button by making it look like a link while maintaining button behavior.</td>
  </tr>
   <tr>
     <td> Success Button</td>
      <td>e-success</td>
      <td>Indicates a successful or positive action.</td>
   </tr>
   <tr>
      <td> Information Button</td>
      <td>e-info</td>
      <td>Indicates a informative sign action to user</td>
   </tr>
   <tr>
   <td>Warning Button</td>
   <td>e-warning</td>
   <td>Indicates the warning action.</td>
   </tr>
   <tr>
   <td>Danger Button</td>
   <td>e-danger</td>
   <td>Indicates the danger sign action to user.</td>
   </tr>
</table>

To customize ejButton as anyone type of custom Buttons ,assign CSS class name of the custom button (For Ex:**e-success**) to cssClass property of ejButton.

The following steps explains you the details about customizing normal ejButton with above mentioned button types.

{% highlight html %}

    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <div class="control">
                        <div class="btnsht">
                            <button id="PrimaryBtn">Primary</button>
                        </div>
                        <div class="btnsht">
                            <button id="DangerBtn">Danger</button>
                        </div>
                        <div class="btnsht">
                            <button id="InfoBtn">Information</button>
                        </div>
                        <div class="btnsht">
                            <button id="WarningBtn">Warning</button>
                        </div>
                        <div class="btnsht">
                            <button id="SuccessBtn">Success</button>
                        </div>
                        <div class="btnsht">
                            <button id="LinkBtn">Link</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
     
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#PrimaryBtn"), {
                size: "medium",
                showRoundedCorner: true,
                cssClass: 'e-primary'
            });
        var basicButton1 = new ej.Button($("#DangerBtn"), {    
                showRoundedCorner: true,
                size: "medium",
                cssClass: 'e-danger'
            });
       var basicButton2 = new ej.Button($("#InfoBtn"), {       
                showRoundedCorner: true,
                size: "medium",
                cssClass: 'e-info'
            });
       var basicButton3 = new ej.Button($("#WarningBtn"), {  
                showRoundedCorner: true,
                size: "medium",
                cssClass: 'e-warning'
            });
       var basicButton4 = new ej.Button($("#LinkBtn"), {      
                size: "medium",
                showRoundedCorner: true,
                cssClass: 'e-link'
            });
       var basicButton5 = new ej.Button($("#SuccessBtn"), {          
                size: "medium",
                showRoundedCorner: true,
                cssClass: 'e-success'
            });
        });
}
{% endhighlight %}

{% highlight css %}

      .frame {
            margin: auto;
            width: 400px;
        }

        .control .btnsht {
            width: 125px;
            display: inline-block;
        }
        .e-btn.e-select.e-btn-medium{
            width:115px;
        }

{% endhighlight %}

Execute the above code to render the following output.

![](Custom-Buttons_images/custom_buttons.png) 

## Image in Button  

The **Essential Studio for JavaScript** has an option of using custom image in a button by assigning a CSS class with background-image to prefixIcon or suffixIcon property of ejButton.Please,refer the following below steps.

Create a custom CSS class with background-image property. Use the following syntax to apply class names.  

**Syntax**: .e-icon .e-[icon name]

{% highlight css %}

    .e-icon .e-profile{
        background-image: url('profile.png');
    }

{% endhighlight %}

{% highlight html %}

    <button id="button">Profile</button>

{% endhighlight %}
Now,assign this custom CSS class name to prefixIcon or suffixIcon property of the ejButton.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ButtonComponent {
    $(function () {
        var basicButton = new ej.Button($("#button"), {
        contentType: "textandimage",
        prefixIcon: "e-icon e-profile",
        size: "large",
        showRoundedCorner: true
    });
  });
}
{% endhighlight %}

Execute the above code to render the following output.

![](Custom-Buttons_images/profile.png)



