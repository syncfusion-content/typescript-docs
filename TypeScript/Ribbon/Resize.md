---
layout: post
title:  Resize
description: resize
documentation: ug
platform: Typescript
keywords: resize,ribbon resize,responsive
---

# Resize 

Ribbon control dynamically resizes to display possible number of controls in the optimal layout as the application window size changes.

As the window is narrowed, controls in the Ribbon will be combined as group button with dropdown arrow, in which controls can be expanded with dropdown arrow.

## Tablet Layout 

Set [`isResponsive`](https://help.syncfusion.com/api/js/ejribbon#members:isresponsive) as true to enable responsive layout in Ribbon.If client width is above  420px or control content exceeds the page then, the ribbon will render in Tablet mode.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbonMenu">
        <li><a>FILE </a>
            <ul>
                <li><a>New</a></li>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "20%",
                // responsive enabled
                isResponsive: true,
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonMenu",
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        content: [{
                            groups: [{
                                id: "cut",
                                text: "Cut"
                            }, {
                                id: "copy",
                                text: "Copy"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }, {
                        text: "Font",
                        content: [{
                            groups: [{
                                id: "bold",
                                text: "Bold"
                            }, {
                                id: "italic",
                                text: "Italic"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }, {
                        text: "Align",
                        content: [{
                            groups: [{
                                id: "left",
                                text: " Left"
                            }, {
                                id: "right",
                                text: "Right"
                            }],
                            defaults: {
                                height: 70,
                                width: 40
                            }
                        }]
                    }]
                }]
            });
        });
}

{% endhighlight %}

![](Resize_images/Resize_img1.png)

## Mobile Layout

If client width is less than 420px, the ribbon will render in mobile mode. In which, you can see that ribbon user interface is customized and redesigned for best view in small screens.
The customized features includes responsive tab & group rendering, backstage, gallery and button controls.

### Responsive Tab and group

Set [`isResponsive`](https://help.syncfusion.com/api/js/ejribbon#members:isresponsive) as true to enable responsive mode in Ribbon.
   

{% highlight html %}

    <div id="Ribbon"></div>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
			isResponsive:true,
                tabs: [{
                    id: "home", text: "HOME", groups: [
                         {
                             text: "Font", alignType: "rows", content: [{
                                 groups: [{
                                     id: "bold",
                                     type: ej.Ribbon.Type.ToggleButton,
                                     isMobileOnly: true,
                                     toggleButtonSettings: {
                                         contentType: ej.ContentType.ImageOnly,
                                         defaultText: "Bold",
                                         activeText: "Bold",
                                         defaultPrefixIcon: "e-icon e-ribbon e-resbold",
                                         activePrefixIcon: "e-icon e-ribbon e-resbold",
                                     }
                                 },
                                    {
                                        id: "italic",
                                        type: ej.Ribbon.Type.ToggleButton,
                                        isMobileOnly: true,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Italic",
                                            activeText: "Italic",
                                            defaultPrefixIcon: "e-icon e-ribbon e-resitalic",
                                            activePrefixIcon: "e-icon e-ribbon e-resitalic",
                                            click: "executeAction"
                                        }
                                    },
                                    {
                                        id: "underline",
                                        text: "Underline",
                                        type: ej.Ribbon.Type.ToggleButton,
                                        isMobileOnly: true,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Underline",
                                            activeText: "Underline",
                                            defaultPrefixIcon: "e-icon e-ribbon e-resunderline",
                                            activePrefixIcon: "e-icon e-ribbon e-resunderline",
                                        }
                                    },
                                    {
                                        id: "strikethrough",
                                        text: "strikethrough",
                                        isMobileOnly: true,
                                        type: ej.Ribbon.Type.ToggleButton,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Strikethrough",
                                            activeText: "Strikethrough",
                                            defaultPrefixIcon: "e-icon e-ribbon strikethrough",
                                            activePrefixIcon: "e-icon e-ribbon strikethrough",
                                        }
                                    },
                                    {
                                        id: "superscript",
                                        text: "superscript",
                                        isMobileOnly: true,
                                        buttonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            prefixIcon: "e-icon e-ribbon e-superscripticon",
                                        }
                                    }
                                 ],
                                 defaults: {
                                     isBig: false
                                 }
                             }]
                         },
					]
                }],
            });
        });
   }

{% endhighlight %}

![](Resize_images/responsive1.png)
{:caption}
Ribbon Responsive with tab content 



N> To make the Ribbon control to react as responsive in mobile devices, it is necessary to refer the additional `ej.responsive.css` file in the application.

## Mobile Toolbar Customization

 Set [`isMobileOnly`](https://help.syncfusion.com/api/js/ejribbon#members:ismobileonly) as true to group control to show the controls 
 in the Mobile Toolbar of the ribbon. For each tab , first row of mobile ribbon will pick and display the controls which is set as `isMobileOnly` with look adapt to mobile mode.If `isMobileOnly` property is not defined to any of the control within tab, then by default first group content will be displayed in first row toolbar.

 To adapt to proper display of controls , following layout will be customized with constants display.

  * First ribbon toolbar and Button controls with min-height. 
  * Drop down control will adapt to full screen width.
  * All button controls icon will be displayed commonly as Top position.
  
  {% highlight html %}

    <div id="Ribbon"></div>

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
			isResponsive:true,
                tabs: [{
                    id: "home", text: "HOME", groups: [
                         {
                             text: "Font", alignType: "rows", content: [{
                                 groups: [{
                                     id: "bold",
                                     type: ej.Ribbon.Type.ToggleButton,
                                     isMobileOnly: true,
                                     toggleButtonSettings: {
                                         contentType: ej.ContentType.ImageOnly,
                                         defaultText: "Bold",
                                         activeText: "Bold",
                                         defaultPrefixIcon: "e-icon e-ribbon e-resbold",
                                         activePrefixIcon: "e-icon e-ribbon e-resbold",
                                     }
                                 },
                                    {
                                        id: "italic",
                                        type: ej.Ribbon.Type.ToggleButton,
                                        isMobileOnly: true,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Italic",
                                            activeText: "Italic",
                                            defaultPrefixIcon: "e-icon e-ribbon e-resitalic",
                                            activePrefixIcon: "e-icon e-ribbon e-resitalic",
                                            click: "executeAction"
                                        }
                                    },
                                    {
                                        id: "underline",
                                        text: "Underline",
                                        type: ej.Ribbon.Type.ToggleButton,
                                        isMobileOnly: true,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Underline",
                                            activeText: "Underline",
                                            defaultPrefixIcon: "e-icon e-ribbon e-resunderline",
                                            activePrefixIcon: "e-icon e-ribbon e-resunderline",
                                        }
                                    },
                                    {
                                        id: "strikethrough",
                                        text: "strikethrough",
                                        type: ej.Ribbon.Type.ToggleButton,
                                        toggleButtonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            defaultText: "Strikethrough",
                                            activeText: "Strikethrough",
                                            defaultPrefixIcon: "e-icon e-ribbon strikethrough",
                                            activePrefixIcon: "e-icon e-ribbon strikethrough",
                                        }
                                    },
                                    {
                                        id: "superscript",
                                        text: "superscript",
                                        buttonSettings: {
                                            contentType: ej.ContentType.ImageOnly,
                                            prefixIcon: "e-icon e-ribbon e-superscripticon",
                                        }
                                    }
                                 ],
                                 defaults: {
                                     isBig: false
                                 }
                             }]
                         },
					]
                }],
            });
        });
  }

{% endhighlight %}

![](Resize_images/responsive2.png)
{:caption}
Ribbon Responsive with MobileToolbar 

### Customized Features

The customized layout for  Quick Access Toolbar, backstage, gallery can be seen following screen shots.
 
 ![](Resize_images/responsive3.png)
 {:caption}
Ribbon Responsive with Quick Access Toolbar 
 
 ![](Resize_images/responsive4.png)
 ![](Resize_images/responsive5.png)
 {:caption}
Ribbon Responsive with backstage
 
 ![](Resize_images/responsive6.png)
 {:caption}
Ribbon Responsive with gallery

## Group Button Customization

Based on window size, detailed group is shrined into single button and you can expand group items with group button click.

For each group shirked for resizing, Custom Class will be added based on group text.For example, `e-action` whereas `action` is group text. Using this custom class, group button can be customized such as to set icons etc.

{% highlight html %}

    <div id="Ribbon"></div>    
    <ul id="ribbonMenu">
        <li>
            <a>FILE</a>
            <ul>
                <li><a>New</a></li>
                <li><a>Open</a></li>
            </ul>
        </li>
    </ul>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
            var fontFamily = ["Segoe UI", "Arial"],
                fontSize = ["1pt", "2pt"];
module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "36%",

                // resizing enabled
                allowResizing: true,
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbonMenu"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Clipboard",
                        alignType: ej.Ribbon.alignType.columns,
                        enableGroupExpander: true,
                        content: [{
                            groups: [{
                                id: "paste",
                                text: "paste",
                                toolTip: "Paste",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-icon e-ribbon e-ribbonpaste"
                                }
                            }],
                            defaults: {
                                isBig: true,
                                width: 50,
                                height: 70
                            }
                        }, {
                            groups: [{
                                id: "cut",
                                text: "Cut",
                                toolTip: "Cut",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    prefixIcon: "e-icon e-ribbon e-ribboncut"
                                }
                            }, {
                                id: "copy",
                                text: "Copy",
                                toolTip: "Copy",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    prefixIcon: "e-icon e-ribbon e-ribboncopy"
                                }
                            }],
                            defaults: {
                                width: 60,
                                height: 40,
                                isBig: false
                            }
                        }]
                    }, {
                        text: "Font",
                        alignType: "rows",
                        content: [{
                            groups: [{
                                id: "fontFamily",
                                toolTip: "Font",
                                dropdownSettings: {
                                    dataSource: fontFamily,
                                    text: "Segoe UI",
                                    width: 150
                                }
                            }, {
                                id: "fontSize",
                                toolTip: "FontSize",
                                dropdownSettings: {
                                    dataSource: fontSize,
                                    text: "1pt",
                                    width: 65
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.type.dropDownList,
                                height: 28,
                                isBig: false,
                            }
                        }]

                    }, {
                        text: "New",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "new",
                                text: "New",
                                toolTip: "New",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-icon e-ribbon e-new"
                                }
                            }],
                            defaults: {
                                width: 60,
                                height: 40
                            }
                        }]
                    }, {
                        text: "Actions",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "undo",
                                text: "Undo",
                                toolTip: "Undo",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-icon e-ribbon e-undo"
                                }
                            }, {
                                id: "redo",
                                text: "Redo",
                                toolTip: "Redo",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-icon e-ribbon e-redo"
                                }
                            }],
                            defaults: {
                                width: 40,
                                height: 70
                            }
                        }]
                    }]
                }, {
                    id: "layout",
                    text: "LAYOUT",
                    groups: [{
                        text: "Print Layout",
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "printLayout",
                                text: "Print Layout",
                                toolTip: "Print Layout",
                                buttonSettings: {
                                    contentType: ej.ContentType.TextAndImage,
                                    imagePosition: ej.ImagePosition.ImageTop,
                                    prefixIcon: "e-icon e-ribbon e-printlayout"
                                }
                            }],
                            defaults: {
                                width: 80,
                                height: 70
                            }
                        }]
                    }]
                }]
            });
        });
    }

    <style type="text/css">
        /*styles set to resize group based on group text custom class*/
        .e-ribbon .e-New:before, .e-ribbon .e-Actions:before {
            font-family: "ej-ribbonfont";
            font-size: 28px;
            line-height: 35px;
        }
        .e-ribbon .e-New:before {
            /*e-New to group “New” */
            content: "\e167";            
            text-indent: -1.5px;
        }
        .e-ribbon .e-Actions:before {
            /*e-Actions to group “Actions”*/
            content: "\e184;
            text-indent: 7px;
        }
    </style>

{% endhighlight %}

![](Resize_images/Resize_img2.png)