---
layout: post
title: Icons-and-navigation
description: icons and navigation
platform: Typescript
control: Menu
documentation: ug
---

# Icons and navigation

##Icons

Icons are the images that is displayed in the **Menu** control. To specify the menu with icons you can use **sprite** property to display the icons. 

Add the following code in your **HTML** page.

{% highlight html %}

        
<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <ul id="menu"></ul>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Initialize the Menu control in JavaScript.
        var data = [
            { id: 1, text: "Group A", parentId: null },
            { id: 2, text: "Group B", parentId: null },
            { id: 3, text: "Group C", parentId: null },
            { id: 4, text: "Group D", parentId: null },
            { id: 5, text: "Group E", parentId: null },
            //first level child
            { id: 11, parentId: 1, text: "Algeria", sprite: "flag-dz" },
            { id: 12, parentId: 1, text: "Armenia", sprite: "flag-am" },
            { id: 13, parentId: 1, text: "Bangladesh", sprite: "flag-bd" },
            { id: 14, parentId: 1, text: "Cuba", sprite: "flag-cu" },
            { id: 15, parentId: 2, text: "Denmark", sprite: "flag-dk" },
            { id: 16, parentId: 2, text: "Egypt", sprite: "flag-eg" },
            { id: 17, parentId: 3, text: "Finland", sprite: "flag-fi" },
            { id: 18, parentId: 3, text: "India", sprite: "flag-in" },
            { id: 19, parentId: 3, text: "Malaysia", sprite: "flag-my" },
            { id: 20, parentId: 4, text: "New Zealand", sprite: "flag-nz" },
            { id: 21, parentId: 4, text: "Norway", sprite: "flag-no" },
            { id: 22, parentId: 4, text: "Poland", sprite: "flag-pl" },
            { id: 23, parentId: 5, text: "Romania", sprite: "flag-ro" },
            { id: 24, parentId: 5, text: "Singapore", sprite: "flag-sg" },
            { id: 25, parentId: 5, text: "Thailand", sprite: "flag-th" },
            { id: 26, parentId: 5, text: "Ukraine", sprite: "flag-ua" },            
        ];

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 425,
            fields: { dataSource: data, id: "id", parentId: "parentId", text: "text", spriteCssClass: "sprite" }
        });
    });
}

{% endhighlight %}


Add the following code in your style section.



{% highlight css %}


<style type="text/css">
        #menu {
            margin-left: 50px;
        }
        .e-menu li > ul > li > a {
            padding: 3px 24px 3px 35px;
        }
        [class^="flag-"],
        [class*="flag-"] {
            background-image: url("../content/images/autocomplete/flags.png");
            height: 14px;
            left: 2px;
            top: 4px;
            width: 24px;
        }
        .flag-am {background-position: -25px 0;}
        .flag-bd {background-position: -75px 0;}
        .flag-cu {background-position: -25px -15px;}
        .flag-dk {background-position: -50px -15px;}
        .flag-dz {background-position: -75px -15px;}
        .flag-eg {background-position: -125px -15px;}
        .flag-fi {background-position: -25px -30px;}
        .flag-id {background-position: -100px -30px;}
        .flag-in {background-position: -125px -30px;}
        .flag-my {background-position: -25px -45px;}
        .flag-no {background-position: -75px -45px;}
        .flag-nz {background-position: -100px -45px;}
        .flag-pl {background-position: -125px -45px;}
        .flag-ro {background-position: -50px -60px;}
        .flag-sg {background-position: -100px -60px;}
        .flag-th {background-position: -125px -60px;}
        .flag-ua {background-position: -25px -75px;}
    </style>


{% endhighlight %}



The following screenshot displays the output for the above code.                                                                                                       

![](Icons-and-navigation_images/Icons-and-navigation_img1.png) 

N> Images for this sample are available in (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\samples\web\content\images<br/>

##Navigation

Navigation in Menu control is the default usage to navigate into the other web page. You can navigate to another page in menu item by providing link to the menu items. Navigation in **Menu** control can be achieved by placing “**href**” path to the anchor tag. Use the following code sample for navigating in **Menu** control.

Add the following code in your **HTML** page.

{% highlight html %}

        
<div>
    <ul id="link">
        <li id="searchengine">
            <a href="#">Search engine</a>
            <ul>
                <li><a href="http://www.bing.com/">Bing</a></li>
                <li><a href="https://www.google.co.in/">Google</a></li>
                <li><a href="https://in.yahoo.com/">Yahoo</a></li>
                <li><a href="http://www.rediff.com/">Rediff</a></li>
            </ul>
        </li>
        <li id="atd"><a href="http://allthingsd.com/">All things digital</a></li>
        <li id="electronics">
            <a>Electronics</a>
            <ul>
                <li>
                    <a href="http://www.engadget.com/">Engadget</a>
                </li>
                <li><a href="http://www.electronista.com/">Electronista</a></li>
                <li><a href="http://www.gearlog.com/">Gearlog</a></li>
            </ul>
        </li>

        <li id="cnet"><a href="http://www.centernetworks.com/">Center networks</a></li>

        <li id="webpronews">
            <a href="http://www.webpronews.com/">Webpronews</a>
        </li>

    </ul>
</div>


{% endhighlight %}

{% highlight javascript %}

 
    // Add the following code in your script section.
    $(function () {
        var sample = new ej.Menu($("#link"),{
             width: 612 });
    });


{% endhighlight %}

The following screenshot displays the output for the above code example.            

![](Icons-and-navigation_images/Icons-and-navigation_img2.png) 


When you click on “**Google**” that is present under “Search engine”, it navigates to the link that you specified in the sample code. Then the output is as follows.

![](Icons-and-navigation_images/Icons-and-navigation_img3.png) 


