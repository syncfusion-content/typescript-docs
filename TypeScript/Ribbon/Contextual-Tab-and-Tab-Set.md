---
layout: post
title:  Contextual-Tab-and-Tab-Set
description: contextual tab and tab set
documentation: ug
platform: Typescript
keywords: contextual tab and tab set
---

# Contextual Tabs

[`Contextual Tabs`](https://help.syncfusion.com/api/js/ejribbon#members:contextualtabs) are collection of Tabs that extended styling and can be shown based on some criteria. Contextual Tabs can be added like [`tabs`](https://help.syncfusion.com/api/js/ejribbon#members:tabs) including groups and content section. You can set [`backgroundColor`](https://help.syncfusion.com/api/js/ejribbon#members:contextualtabs-backgroundcolor) and [`borderColor`](https://help.syncfusion.com/api/js/ejribbon#members:contextualtabs-bordercolor) to highlight them as Tab set. Contextual tabs can be added or set dynamically in ribbon control using [`addContextualTabs`](https://help.syncfusion.com/api/js/ejribbon#methods:addcontextualtabs) with it's object and index position.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbon">
            <li>
                <a>FILE</a>
                <ul>
                    <li><a>New</a></li>
                </ul>
            </li>
        </ul>
        <div id="Contents">Custom Control</div>
        <div id="headings" class="e-headings">
            <div>
                <p>Ribbon-Heading</p>
                <p>No Spacing</p>
            </div>
            <div>
                <p class="e-strong">Ribbon Heading</p>
                <p>Strong</p>
            </div>
            <div>
                <p class="e-emphasis">Ribbon Heading</p>
                <p>Emphasis</p>
            </div>
        </div>
        <table id="design" class="e-designtablestyle">
            <tr>
                <td>
                    <input type="checkbox" id="Check2" />
                    <label for="Check2">First Column</label>
                </td>
                <td>
                    <input type="checkbox" id="check4" checked="checked" />
                    <label for="check4">Total Row</label>
                </td>
            </tr>
        </table>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                    width: "500px",
                    applicationTab: {
                        type: ej.Ribbon.applicationTabType.menu,
                        menuItemID: "ribbon"
                    },
                    tabs: [{
                        id: "home",
                        text: "HOME",
                        groups: [{
                            text: "CustomControls",
                            type: "custom",
                            contentID: "Contents"
                        }]
                    }],
    
                    // contextual Tabs collection
                    contextualTabs: [{
    
                        // contextual tab with custom content
                        backgroundColor: "#FCFBEB",
                        borderColor: "#F2CC1C",
                        tabs: [{
                            id: "Design",
                            text: "DESIGN",
                            groups: [{
                                text: "Table Style Options",
                                type: "custom",
                                contentID: "design"
                            }]
                        }]
                    },
    
                        // tab set with background & border color
                        {
                            backgroundColor: "blue",
                            borderColor: "lightblue",
                            tabs: [{
                                id: "tabset1",
                                text: "Tabset1",
                                groups: [{
                                    text: "Tabset1 Style",
                                    type: "custom",
                                    contentID: "headings"
                                }]
                            }, {
                                id: "tabset2",
                                text: "Tabset2",
                                groups: [{
                                    text: "TabSet2 Style",
                                    content: [{
                                        // groups with button controls
                                        groups: [{
                                            id: "uppercase",
                                            text: "Upper Case",
                                            buttonSettings: {
                                                contentType: ej.ContentType.ImageOnly,
                                                prefixIcon: "e-icon e-ribbon e-uppercase"
                                            }
                                        }, {
                                            id: "lowercase",
                                            text: "Lower Case",
                                            buttonSettings: {
                                                contentType: ej.ContentType.ImageOnly,
                                                prefixIcon: "e-icon e-ribbon e-lowercase"
                                            }
                                        }],
                                        defaults: {
                                            isBig: true
                                        }
                                    }]
                                }]
                            }]
                        }
                    ]
                });
            });
  }

{% endhighlight %}


![](Contextual-Tab-and-Tab-Set_images/Contextual-Tab-and-Tab-Set_img1.png)

