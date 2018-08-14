---
layout: post
title:  Tab
description: tab 
documentation: ug
platform: Typescript
keywords: ribbon tab
---

# Tab

Tab is a collection of control [`groups`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups) which enables you to organize related commands into single view.  Tabs can be added to Ribbon using [`tabs`](https://help.syncfusion.com/api/js/ejribbon#members:tabs) property. [`id`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-id) & [`text`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-text) properties are used to set unique ID and header text to Tab.
The manipulation of given text tab in the ribbon control can be done by using  [`addTab`](https://help.syncfusion.com/api/js/ejribbon#methods:addtab), [`removeTab`](https://help.syncfusion.com/api/js/ejribbon#methods:removetab), [`hideTab`](https://help.syncfusion.com/api/js/ejribbon#methods:hidetab),
[`showTab`](https://help.syncfusion.com/api/js/ejribbon#methods:showtab) methods and [`tabAdd`](https://help.syncfusion.com/api/js/ejribbon#events:tabadd), [`tabCreate`](https://help.syncfusion.com/api/js/ejribbon#events:tabcreate), [`tabRemove`](https://help.syncfusion.com/api/js/ejribbon#events:tabremove), [`tabClick`](https://help.syncfusion.com/api/js/ejribbon#events:tabclick) and [`tabSelect`](https://help.syncfusion.com/api/js/ejribbon#events:tabselect) events.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbonMenu">
        <li>
            <a>FILE</a>
            <ul>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
    <div id="sendReceive">
        Send/Receive All Folders
    </div>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "500px",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonMenu"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Save",
                        content: [{
                            groups: [{
                                text: "Save",
                                isBig: true,
                                buttonSettings: {
                                    prefixIcon: "e-icon e-save",
                                    contentType: ej.ContentType.ImageOnly
                                }
                            }]
                        }]
                    }, {
                        text: "Print",
                        content: [{
                            groups: [{
                                text: "Print",
                                isBig: true,
                                type: ej.Ribbon.type.toggleButton,
                                toggleButtonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    defaultText: "Print",
                                    activeText: "Print",
                                    defaultPrefixIcon: "e-icon e-print",
                                    activePrefixIcon: "e-icon e-print",
                                }
                            }]
                        }]
                    }]
                }, {
                    id: "sendRec",
                    text: "Send/Receive",
                    groups: [{
                        type: "custom",
                        contentID: "sendReceive"
                    }]
                }]
            });
        });
  }

   
{% endhighlight %}

![](Tab_images/Tab_img1.png)