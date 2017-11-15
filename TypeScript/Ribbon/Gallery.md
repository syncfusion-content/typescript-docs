---
layout: post
title: Gallery
description: gallery
documentation: ug
platform: Typescript
keywords: gallery,ribbon gallery
---

# Gallery

Galleries are used to display items that can be arranged in a grid-type layout. Items in the gallery can be customized as [`button`](https://help.syncfusion.com/api/js/ejbutton)/[`menu`](https://help.syncfusion.com/api/js/ejmenu) to display images, text, or both images and text. You can set [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type) of group as `gallery`.

## Gallery Items

[`Gallery items`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-galleryitems) are collection of the items to be included in the main gallery. You can set [`text`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-galleryitems-text) and [`toolTip`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-galleryitems-tooltip) to gallery item which can also be customized with [`buttonSettings`](https://help.syncfusion.com/api/js/ejbutton).
 
Number of [`columns`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-columns) to display in gallery for each row should be specified and the Number of columns in Expanded State [`(expandedColumns)`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-expandedcolumns) can be customized, if not set, `columns` count will be set as default. 

N> The [`itemHeight`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-itemheight) and [`itemWidth`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-itemwidth) for gallery item can be set, if not set default values will be used.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbon">
        <li><a>FILE</a>
            <ul>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "500",
                applicationTab: {
                    type:ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbon"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        type: "gallery",
                        text: "Gallery",
                        content: [{
                            groups: [{
                                id: "Gallery",
                                columns: 2,
                                itemHeight: 54,
                                itemWidth: 73,
                                expandedColumns: 3,
                                type: ej.Ribbon.type.gallery,
                                galleryItems: [{
                                    text: "GalleryContent1",
                                    toolTip: "GalleryContent1",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent1 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent2",
                                    toolTip: "GalleryContent2",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent2 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent3",
                                    toolTip: "GalleryContent3",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent3 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent4",
                                    toolTip: "GalleryContent4",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent4 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }]
                            }]
                        }]
                    }]
                }]
            });
        });
}
    <style type="text/css">
        .e-gallerycontent1 {
            background-position: 0 -105px;
        }
        .e-gallerycontent2 {
            background-position: -69px -105px;
        }
        .e-gallerycontent3 {
            background-position: -136px -105px;
        }
        .e-gallerycontent4 {
            background-position: 0 -53px;
        }
        .e-gbtnposition {
            margin-top: 5px;
        }
        .e-gbtnimg {
            background-image: url("../themes/common-images/ribbon/homegallery.png");
            background-repeat: no-repeat;
            height: 64px;
            width: 64px;
        }
    </style>


{% endhighlight %}


![](Gallery_images/Gallery_img1.png)

Ribbon Gallery.
{:.caption}


![](Gallery_images/Gallery_img2.png)

Gallery at Expanded State
{:.caption}

## Custom Gallery Items

[`Custom gallery items`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customgalleryitems) are the additional items to be displayed at gallery expanded state. You can set [`customItemType`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customgalleryitems-customitemtype) as `button` or `menu`, Default is `button`.

You can also set [`text`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customgalleryitems-text) and [`toolTip`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customgalleryitems-tooltip) to custom gallery item which can also be customized with [`buttonSettings`](https://help.syncfusion.com/api/js/ejbutton)/[`menuSettings`](https://help.syncfusion.com/api/js/ejmenu) based on the [`customItemType`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customgalleryitems-customitemtype) specified.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbon">
        <li><a>FILE</a> </li>
    </ul>
    <ul id="customMenu">
        <li>
            <a>New Quick Step</a>
            <ul>
                <li><a>Flag and Move</a></li>
            </ul>
        </li>
    </ul>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "500",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbon"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        type: "gallery",
                        text: "Gallery",
                        content: [{
                            groups: [{
                                id: "Gallery",
                                columns: 2,
                                itemHeight: 54,
                                itemWidth: 73,
                                expandedColumns: 3,
                                type: ej.Ribbon.type.gallery,
                                galleryItems: [{
                                    text: "GalleryContent1",
                                    toolTip: "GalleryContent1",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent1 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent2",
                                    toolTip: "GalleryContent2",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent2 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent3",
                                    toolTip: "GalleryContent3",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent3 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }, {
                                    text: "GalleryContent4",
                                    toolTip: "GalleryContent4",
                                    buttonSettings: {
                                        contentType: ej.ContentType.ImageOnly,
                                        prefixIcon: "e-icon e-gallerycontent4 e-gbtnimg",
                                        cssClass: "e-gbtnposition"
                                    }
                                }],
                                customGalleryItems: [{
                                    customItemType: ej.Ribbon.customItemType.menu,
                                    menuId: "customMenu",
                                    menuSettings: {
                                        openOnClick: false
                                    }
                                }, {
                                    text: "Clear Formatting",
                                    toolTip: "Clear Formatting",
                                    customItemType: ej.Ribbon.customItemType.button,
                                    buttonSettings: {                                        
                                        cssClass: "e-extrabtnstyle"
                                    }
                                }]
                            }]
                        }]
                    }]
                }]
            });
        });
}
    <style type="text/css">
        .e-gallerycontent1 {
            background-position: 0 -105px;
        }
        .e-gallerycontent2 {
            background-position: -69px -105px;
        }
        .e-gallerycontent3 {
            background-position: -136px -105px;
        }
        .e-gallerycontent4 {
            background-position: 0 -53px;
        }
        .e-gbtnposition {
            margin-top: 5px;
        }
        .e-gbtnimg {
            background-image: url("../themes/common-images/ribbon/homegallery.png");
            background-repeat: no-repeat;
            height: 64px;
            width: 64px;
        }
        .e-extracontent .e-extrabtnstyle {
            padding-left: 28px;
            text-align: left;
        }
    </style>

{% endhighlight %}

![](Gallery_images/Gallery_img3.png)