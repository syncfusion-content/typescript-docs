---
layout: post
title: Syncfusion Grouped-List
description: grouped list
platform: Typescript
control: ListView
documentation: ug
---

# Grouped List

**First Level Group List**

The **ListView** widget can make as grouped list by setting the **“data-ej-enableGroupList”** attribute as **“True”**. This groups the set of items listed under **ul**. You can identify the grouped items with the header title specified respectively.

Refer the following code example.



{% highlight html %}

    <div id="defaultListView" >
        <ul data-ej-grouplisttitle="Network">
            <li data-ej-text="Airplane Mode"></li>
            <li data-ej-text="Wi-Fi"></li>
            <li data-ej-text="Notifications"></li>
            <li data-ej-text="Location Services"></li>
        </ul>
        <ul data-ej-grouplisttitle="Apps">
            <li data-ej-text="Sound"></li>
            <li data-ej-text="Music"></li>
            <li data-ej-text="Brightness"></li>
            <li data-ej-text="Wallpaper"></li>
        </ul>
        <ul data-ej-grouplisttitle="Settings">
            <li data-ej-text="General"></li>
            <li data-ej-text="Brightness"></li>
            <li data-ej-text="Wallpaper"></li>
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
                 width:400, 
                 enableGroupList:true 
            });
        });
}

{% endhighlight %}



Run the codes to get the following output

![Grouped List](Grouped-List_images/Grouped-List_img1.png) 


**Nested Child Group List**

While selecting a list item that is grouped, you can also render another set of list items. This is achieved by defining the desired **child item list** within the list containing **`PrimaryKeyValue`.** This **[`data-ej-primarykey`]** attribute relates the parent child for identifying its appropriate child when clicking on the parent list item.

Refer the following code examples.



{% highlight html %}


    <div id="defaultListView" >
        <ul data-ej-grouplisttitle="Network">
            <li data-ej-text="Airplane Mode"></li>
            <li data-ej-text="Wi-Fi"></li>
            <li data-ej-text="Notifications"></li>
            <li data-ej-text="Location Services"></li>
        </ul>
        <ul data-ej-grouplisttitle="Apps">
            <li data-ej-primarykey="1" data-ej-text="Sound">
                <ul>
                    <li data-ej-text="Ring Tone"></li>
                    <li data-ej-text="Message Tone"></li>
                    <li data-ej-text="Notification Tone"></li>
                </ul>
            </li>
            <li data-ej-text="Brightness"></li>
            <li data-ej-text="Wallpaper"></li>
        </ul>
        <ul data-ej-grouplisttitle="Settings">
            <li data-ej-text="General"></li>
            <li data-ej-text="Brightness"></li>
            <li data-ej-text="Wallpaper"></li>
        </ul>

    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#defaultListView"), {
                showHeader: true, 
                headerTitle: "Favorite",
                width:400, 
                enableGroupList:true
            });
        });
    }

{% endhighlight %}



Run the codes to get the following output

![Grouped](Grouped-List_images/Grouped-List_img2.png) 

