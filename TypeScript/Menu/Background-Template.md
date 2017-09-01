---
layout: post
title: Background-Template
description: background template
platform: Typescript
control: Menu
documentation: ug
---

# Background Template

**Menu** control also provides support for template support. Normally **Menu** control can be created by using **UL** and **LI** tags in the preferred way. But in template supporting, you can customize the appearance of sub menu items rendering. 

Initialize the Template **Menu** as illustrated in the following code example. 

Add the following code in your **HTML** page.

{% highlight html %}


<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <ul id="template">
                <li>
                    <a>My Computer</a>
                    <ul>
                        <li>
                            <div class="temp temp1">
                                <span>Disks</span>
                                <ul>
                                    <li><a>Local Disk : C</a></li>
                                    <li><a>Local Disk : D</a></li>
                                </ul>
                                <ul>
                                    <li><a>Local Disk : E</a></li>
                                    <li><a>Local Disk : F</a></li>
                                </ul>
                            </div>
                        </li>
                    </ul>
                </li>
                <li>
                    <a>Libraries</a>
                    <ul>
                        <li>
                            <div class=" temp temp2">
                                <div>
                                    <span>Documents</span>
                                    <ul>
                                        <li><a>Images</a></li>
                                        <li><a>Videos</a></li>
                                    </ul>
                                    <ul>
                                        <li><a>Documents</a></li>
                                        <li><a>Music</a></li>
                                    </ul>
                                </div>
                            </div>
                        </li>
                    </ul>
                </li>

                <li>
                    <a>Favorites </a>
                    <ul>
                        <li>
                            <div class="temp temp3">
                                <div>
                                    <span>Favorites</span>
                                    <ul>
                                        <li><a>Downloads</a></li>
                                        <li><a>Recent Places</a></li>
                                    </ul>
                                    <ul>
                                        <li><a>Desktop</a></li>
                                    </ul>
                                </div>
                            </div>
                        </li>
                    </ul>
                </li>
                <li>
                    <a>Gaming</a>
                    <ul>
                        <li>
                            <div class="temp temp4">
                                <div>
                                    <span>GAMING</span>
                                    <ul>
                                        <li><a>Upcoming</a></li>
                                        <li><a>Consoles</a></li>
                                    </ul>
                                    <ul>
                                        <li><a>FIFA 2999</a></li>
                                        <li><a>Carom legend</a></li>
                                    </ul>
                                </div>
                            </div>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#template"),{
    });
 });
}
{% endhighlight %}



Add the following code in your style section.

{% highlight css %}


<style type="text/css">
    .temp {
        height: 237px;
        width: 375px;
        font-family: segoe UI;
        cursor: default;
        background-size: 100% 100%;
    }

    .temp span {
        color: red;
        float: left;
        font-size: 20px;
        left: 20px;
        position: relative;
        top: 25px;
        width: 100px;
    }

    .temp ul {
        float: left;
        font-size: 14px;
        left: -79px;
        list-style-type: none;
        margin: 0;
        padding: 0;
        position: relative;
        top: 50px;
        width: 128px;
    }

    .temp ul li {
        font-size: 13px;
    }

    .temp ul li a {
        text-decoration: underline;
        cursor: pointer;
        color: #000;
    }

    .temp1 {
        background-image: url("1.jpg");
    }

    .temp2 {
        background-image: url("2.jpg");
    }

    .temp3 {
        background-image: url("3.jpg");
    }

    .temp4 {
        background-image: url("4.jpg");
    }

    .e-menu.e-horizontal li > ul, .e-menu.e-horizontal li > ul > li:hover {
        background-color: #fff;
    }

    .e-menu.e-horizontal > li > ul:after {
        border-color: transparent transparent #fff;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.                       

![](Background-Template_images/Background-Template_img1.png) 



