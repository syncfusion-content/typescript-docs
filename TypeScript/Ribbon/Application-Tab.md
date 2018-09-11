---
layout: post
title:  Ribbon-Application-Tab
description: application tab
documentation: ug
platform: Typescript
keywords: application tab,ribbon application tab
---

# Application Tab

The Application Tab is used to represent a `Menu` that do some operations, such as File menu to create, open, and print documents. Application Tab classified by [`type`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-type) property with the following:

*  menu
*  backstage

## Application Menu

The Application Menu is similar to traditional file menu options and Syncfusion `ejMenu` control is used internally to render this. To show Application Menu in Ribbon, set the [`type`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-type) as `menu` and [`menuSettings`](https://help.syncfusion.com/api/js/ejmenu) to customize properties of `ejMenu`.

### _Create Using Template_

Set the UL element `id` to [`menuItemID`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-menuitemid) property to create Application Menu and it will acts as template to render menu.

{% highlight html %}
    
        <div id="Ribbon"></div>
        <!--UL template to render menu-->
        <ul id="ribbon">
        <li>
            <a>FILE</a>
            <ul>
            <li><a>Open</a></li>
            <li><a>Print</a></li>
            </ul>
        </li>
        </ul>
        <div id="Contents">Custom control</div>

 /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

 module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                    width: "500px",
                    applicationTab: {
                        type: ej.Ribbon.applicationTabType.menu,
                        // menuItemID mapped to UL with id of “menu”                                         
                        menuItemID: "ribbon",
                        // menu properties defined in menu settings 
                        menuSettings: {
                            openOnClick: false
                        }
                    },
                    tabs: [{
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "New",
                            type: "custom",
                            contentID: "Contents"
                        }]
                    }]
               });
         });
    }

{% endhighlight %}

![](Application-Tab_images/Application-Tab_img1.png)

### _Binding Data Source_

Application Menu can be rendered using JSON Data Source. Please refer [`this`](https://help.syncfusion.com/js/menu/data-binding) page to set data source to `ejMenu`.

{% highlight html %}
    
    <div id="Ribbon"></div>
    <ul id="ribbon">
    </ul>

 /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

 module RibbonComponent {
        var data = [{
            id: 1,
            text: "File",
            parentId: null
        }, {
            id: 11,
            parentId: 1,
            text: "Open"
        }, {
            id: 12,
            parentId: 1,
            text: "Save"
        }, {
            id: 121,
            parentId: 12,
            text: "Save As"
        }, {
            id: 122,
            parentId: 12,
            text: "Save All"
        }];
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: 500,
                applicationTab: {
                    type:ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbon",
                    menuSettings: {
                        // data source to menu
                        fields: {
                            dataSource: data,
                            id: "id",
                            parentId: "parentId",
                            text: "text"
                        }
                    }
                },
                tabs: [{
                    id: "home",
                    text: "Home",
                    groups: [{
                        text: "Font",
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold",
                                isBig: true,
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-icon e-ribbon e-bold"
                                }
                            }]
                        }]
                    }]
                }]
            });
        });
   }


{% endhighlight %}

![](Application-Tab_images/Application-Tab_img2.png)

## Backstage Page

The Backstage page is where documents and related data of those can be managed, such as Create, Save and other information.

The Backstage page has a feature to add custom Control in left side of the page which contains menu items and the right side contains corresponding user controls. 

You can set Application Tab [`type`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-type) as `backstage` and set [`id`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages-id) , [`text`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages-text) to backstage items. Backstage [`pages`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages) can be added with required [`itemType`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages-itemtype) and [`contentID`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages-contentid) as template id to render template into Backstage. 

Separator between Backstage items can be enabled by setting [`enableSeparator`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-pages-enableseparator) as true. Width of back stage side header can be customized using [`headerWidth`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-headerwidth), If not set based on content given width will be considered.

To render the Ribbon with the Backstage page, refer to the following code snippet.

{% highlight html %}
    <div id="Ribbon"></div>
    <div id="newCon">
        <table>
            <tr>
                <td>
                    <button id="btn1" class="e-bsnewbtnstyle">Blank WorkBook</button></td>
            </tr>
        </table>
    </div>
    <div id="accountCon">
        <div class="e-userDiv">
            <span>User Information</span>
            <div>
                <div class="e-accuser e-newpageicon"></div>
                <div class="e-userCon">
                    <div>user</div>
                    <div>any@syncfusion.com</div>
                </div>
            </div>
        </div>
        <a href="#">Sign out</a>
    </div>
    <div id="ribbonContent">Home control</div>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var button = new ej.Button($("#btn1"), {
            size: "large",
            height: 200,
            width: 205,
            contentType: "textandimage",
            imagePosition: "imagetop",
            prefixIcon: "e-icon e-blank e-infopageicon"
        });
           var sample = new ej.Ribbon($("#Ribbon"), {
                width: "500px",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.backstage,
                    text: "FILE",
                    // height and width of bask stage is set 
                    backstageSettings: {
                        text: "FILE",
                        height: 360,
                        width: 600,
                        headerWidth: 125,
                        pages: [{
                            // id and text of bask stage item

                            id: "new",
                            text: "New",
                            contentID: "newCon"
                        }, {
                            id: "close",
                            text: "Close",
                            // enable separator is to set separator between backstage items

                            enableSeparator: true,
                            backStageItemType: ej.Ribbon.itemType.button
                        }, {
                            id: "account",
                            text: "Office Account",
                            contentID: "accountCon"
                        }]
                    }
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "New",
                        type: "custom",
                        contentID: "ribbonContent"
                    }]
                }]
            });
        });
}
    <style type="text/css">
        .e-accuser {
            background-image: url"../themes/common-images/ribbon/User.jpg");
        }
        .e-blank {
            background-image: url("../themes/common-images/ribbon/blank.png");
        }
        .e-infopageicon {
            background-repeat: no-repeat;
            height: 150px;
            width: 198px;
        }
        .e-newpageicon {
            background-repeat: no-repeat;
            height: 42px;
            width: 42px;
        }
        .e-bspagestyle {
            line-height: 0;
            font-size: 30px;
        }
        .e-ribbon .e-ribbonbackstagepage .e-bsnewbtnstyle {
            color: #212121;
            background: #fdfdfd;
            margin: 20px;
        }
    </style>

{% endhighlight %}

![](Application-Tab_images/Application-Tab_img3.png)

N> Height & width of backstage can be set using [`height`](https://help.syncfusion.com/api/js/ejribbon#members:applicationtab-backstagesettings-height) and `width`, if these are not set, Ribbon’s height & width will be considered.

You can add/remove/update backStage item to the ribbon control by using [`addBackStageItem`](https://help.syncfusion.com/api/js/ejribbon#methods:addbackstageitem), [`removeBackStageItem`](https://help.syncfusion.com/api/js/ejribbon#methods:removebackstageitem) and [`updateBackStageItem`](https://help.syncfusion.com/api/js/ejribbon#methods:updatebackstageitem) methods. Also you can show/hide the backstage page in ribbon control by using [`showBackstage`](https://help.syncfusion.com/api/js/ejribbon#methods:showbackstage) and [`hideBackstage`](https://help.syncfusion.com/api/js/ejribbon#methods:hidebackstage methods.