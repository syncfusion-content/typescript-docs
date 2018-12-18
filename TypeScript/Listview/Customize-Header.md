---
layout: post
title: Syncfusion Customize-Header
description: customize header
platform: Typescript
control: ListView
documentation: ug
---

# Customize Header

In **ListView**, you can enable the built-in **Header** support. To show or hide the **Header** in **ListView**, use the [`data-ej-showheader`] attribute. By default, **ListView** is rendered with the **Header**. You can set the title for the **Header** by using the [`data-ej-headertitle`]attribute.

In some cases, for the purpose of navigation, you may want to show the **Back** button in **ListView Header**. To achieve this, [`data-ej-showheaderbackbutton`] attribute is used. By default, **ListView** is not rendered with the header back button in parent page. To customize the text shown in **ListView Header Back** button, the attribute [`data-ej-headerbackbuttontext`] is used. 

Refer the following code example.



{% highlight html %}


        <div id="defaultListView">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}
 
/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#defaultListView"), {
                showHeader:true,
                showHeaderBackButton:true, 
                headerBackButtonText :"Menu",
                width:400
            });
        });
}

{% endhighlight %}



Run the code to get the following output

![Header](Customize-Header_images/Customize-Header_img1.png) 

