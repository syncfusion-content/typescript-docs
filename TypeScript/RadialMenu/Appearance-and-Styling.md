---
layout: post
title: Appearance and Styling | AutoComplete | Syncfusion
description: appearance and styling
platform: Typescript
control: RadialMenu
documentation: ug
---

# Appearance and Styling

You can customize RadialMenu control style and the appearance by using available themes or cssClass property.

## Theme

In order to apply styles to the RadialMenu control, refer these 2 files namely, ej.widgets.core.min.css and ej.theme.min.css. When you refer ej.web.all.min.css file, it is not necessary to include the files ej.widgets.core.min.css and ej.theme.min.css in your project, as ej.web.all.min.css is the combination of these two. 

By default, there are 16 theme support available for RadialMenu component, namely:

* flat-azure
* flat-azure-dark
* fat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap
* high-contrast-01
* high-contrast-02
* material
* office-365

## CSS Class

RadialMenu component's appearance can only be customized using its CSS classes. Define CSS class, as per requirement and assign the class name to cssClass property.

### Configure RadialMenu using CSS class

Define CSS class to customize the RadialMenu control.


{% highlight css %}

    <style type="text/css">

            /* Customize the radialmenu */

        .e-radialmenu .e-default, .e-radialmenu .e-outerdefault.customCss 

        {

                fill:#f00;
        } 
    </style>

{% endhighlight %}



In the HTML page, define the li items for RadialMenu component.

{% highlight html %}

    <div id="radialmenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/copy.png"
                data-ej-text="Copy">
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/paste.png"
                data-ej-text="Paste">
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/redo.png"
                data-ej-text="Redo">
            </li>
            <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/undo.png"
                data-ej-text="Undo">
            </li>
        </ul>
    </div>

{% endhighlight %}


Initialize the **Radial Menu** control with cssClass in the script as follows.


{% highlight javascript %}
  
module RadialMenuComponent {
    $(function () {
         var radialmenuInstance = new ej.RadialMenu($("#radialmenu"), {
                 cssClass: "customCss" 
                 });
        });
}  

{% endhighlight %}


Output of RadialMenu configured based on CSS class is as follow,


![](apperance-and-styling-images\appearance-and-styling_img1.png)


