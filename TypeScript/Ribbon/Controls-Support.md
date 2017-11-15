---
layout: post
title: Controls-Support
description: controls support
documentation: ug
platform: Typescript
keywords: controls support,ribbon controls support
---

# Controls Support

Button, Split Button, DropdownList, Toggle button, Gallery and Custom controls can be added to each groups. You can set [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type) property in group to define the controls. Default `type` is `button`. 

## Built in Controls

The following table describes about the built in controls [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type) and their corresponding control settings.

<table class="params">
<thead>
<tr>
<th>Type</th>
<th>Control Settings</th>
<th class="last">Example</th>
</tr>
</thead>                     
<tbody>
<tr>
<td class="type">Button</td>
<td class="control settings"><span class="param-type"><a href="https://help.syncfusion.com/api/js/ejbutton">ejButton</a> -  <a href="https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-buttonsettings">buttonSettings</a></span></td><td class="example last">
    buttonSettings: {
					width: 70,
					contentType: ej.ContentType.ImageOnly,
					prefixIcon: "e-icon e-ribbon e-new"
				    }                           
 </td>
</tr>
<tr>
<td class="type">SplitButton</td>
<td class="control settings"><span class="param-type"> <a href="https://help.syncfusion.com/api/js/ejsplitbutton">ejSplitButton</a> - <a href="https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-splitbuttonsettings">splitButtonSettings</a></span></td>
<td class="example last">
	splitButtonSettings: {
                          contentType: ej.ContentType.ImageOnly,
                          targetID: "pasteSplit",
                          buttonMode: "dropdown",
                          arrowPosition: ej.ArrowPosition.Bottom
                          }
 </td>
</tr>
<tr>
<td class="type">ToggleButton</td>
<td class="control settings"><span class="param-type"><a href="https://help.syncfusion.com/api/js/ejtogglebutton">ejToggleButton</a> - <a href="https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-togglebuttonsettings">toggleButtonSettings</a></span></td>
<td class="example last">
	toggleButtonSettings: {
                           contentType: ej.ContentType.ImageOnly,
                           defaultText: "Italic",
                           activeText: "Italic",
                           }
 </td>
</tr>
<tr>
<td class="type">DropDownList</td>
<td class="control settings"><span class="param-type"><a href="https://help.syncfusion.com/api/js/ejdropdownlist">ejDropDownList</a> - <a href="https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-dropdownsettings">dropdownSettings</a></span></td>
<td class="example last">
	dropdownSettings: {
                      dataSource: size,
                      text: "1pt",
                      width: 65
                      }
 </td>
</tr>
</tbody>
</table>

N> 1. You can specify type either to [`group’s collection`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults) or to each [`group`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type).
N> 2. For [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type) property you can assign either string value (“splitbutton”) or enum value (ej.Ribbon.type.splitButton).

{% highlight html %}

	<div id="Ribbon"></div>
    <ul id="ribbon">
                    <li><a>FILE</a>
                        <ul>
                            <li><a>New</a></li>
                        </ul>
                    </li>
                </ul>
                <ul id="pasteSplit">
                    <li><a>Paste</a></li>
                </ul>


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

        var fontFamily = ["Segoe UI", "Arial", "Times New Roman", "Tahoma", "Helvetica"], fontSize = ["1pt", "2pt", "3pt", "4pt", "5pt"], action1 = ["New", "Clear"], action2 = ["Bold", "Italic", "Underline", "strikethrough", "superscript", "subscript", "JustifyLeft", "JustifyCenter", "JustifyRight", "JustifyFull", "Undo", "Redo"];
module RibbonComponent {
    $(function () {
                width: "100%",
                applicationTab: { Type: ej.Ribbon.applicationTabType.menu, menuItemID: "ribbon", menuSettings: { openOnClick: false } },
                tabs: [
                    {
                        id: "home",
                        text: "HOME",
                        groups: [
                            {
                                text: "New",
                                alignType: ej.Ribbon.alignType.rows,
                                content: [
                                    {
                                        groups: [
                                            {
                                                id: "new",
                                                text: "New",
                                                toolTip: "New",
                                                buttonSettings: {
                                                    contentType: ej.ContentType.ImageOnly,
                                                    imagePosition: ej.ImagePosition.ImageTop,
                                                    prefixIcon: "e-icon e-ribbon e-new"
                                                }
                                            }
                                        ],
                                        defaults: {
                                            type: ej.Ribbon.type.button,
                                            width: 60,
                                            height: 70
                                        }
                                    }
                                ]
                            },
                            {
                                text: "Clipboard",
                                alignType: ej.Ribbon.alignType.columns,
                                content: [
                                    {
                                        groups: [
                                            {
                                                id: "paste",
                                                text: "paste",
                                                toolTip: "Paste",
                                                splitButtonSettings: {
                                                    contentType: ej.ContentType.ImageOnly,
                                                    prefixIcon: "e-icon e-ribbon e-ribbonpaste",
                                                    targetID: "pasteSplit",
                                                    buttonMode: "dropdown",
                                                    arrowPosition: ej.ArrowPosition.Bottom
                                                }
                                            }
                                        ],
                                        defaults: {
                                            type: ej.Ribbon.type.splitButton,
                                            width: 50,
                                            height: 70
                                        }
                                    }
                                ]
                            },
                            {
                                text: "Font",
                                alignType: "rows",
                                content: [
                                    {
                                        groups: [
                                            {
                                                id: "fontFamily",
                                                toolTip: "Font",
                                                dropdownSettings: {
                                                    dataSource: fontFamily,
                                                    text: "Segoe UI",
                                                    width: 150
                                                }
                                            },
                                            {
                                                id: "fontSize",
                                                toolTip: "FontSize",
                                                dropdownSettings: {
                                                    dataSource: fontSize,
                                                    text: "1pt",
                                                    width: 65
                                                }
                                            }
                                        ],
                                        defaults: {
                                            type: ej.Ribbon.type.dropDownList,
                                            height: 28
                                        }
                                    }, {
                                        groups: [
                                            {
                                                id: "bold",
                                                toolTip: "Bold",
                                                type: ej.Ribbon.type.toggleButton,
                                                toggleButtonSettings: {
                                                    contentType: ej.ContentType.ImageOnly,
                                                    defaultText: "Bold",
                                                    activeText: "Bold",
                                                    defaultPrefixIcon: "e-icon e-ribbon bold",
                                                    activePrefixIcon: "e-icon e-ribbon bold"
                                                }
                                            },
                                            {
                                                id: "italic",
                                                toolTip: "Italic",
                                                type: ej.Ribbon.type.toggleButton,
                                                toggleButtonSettings: {
                                                    contentType: ej.ContentType.ImageOnly,
                                                    defaultText: "Italic",
                                                    activeText: "Italic",
                                                    defaultPrefixIcon: "e-icon e-ribbon e-ribbonitalic",
                                                    activePrefixIcon: "e-icon e-ribbon e-ribbonitalic"
                                                }
                                            }
                                        ],
                                        defaults: {
                                            isBig: false,
                                        }
                                    }
                                ]
                            }
                        ],
                    }
                ],
        });
   }
   
{% endhighlight %}

![](Controls-Support_images/Controls-Support_img1.png)

## Custom

You can set [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-type) as `custom` to render custom controls and Custom element id has to be specified as [`contentID`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-contentid).You can change the element defined in the custom template to appropriate Syncfusion control in the event of Ribbon [`create`](https://help.syncfusion.com/api/js/ejribbon#events:create).

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbon">
        <li>
            <a>FILE </a>
            <ul>
                <li><a>New</a></li>
                <li><a>Print</a></li>
            </ul>
        </li>
    </ul>
    <input id="fontColor" />
    <table id="design" class="e-designtablestyle">
        <tr>
            <td>
                <input type="checkbox" id="check1" /><label for="check1">Header Row</label></td>
            <td>
                <input type="checkbox" id="Check2" checked="checked" /><label for="Check2">First Column</label></td>
        </tr>
        <tr>
            <td>
                <input type="checkbox" id="check4" checked="checked" /><label for="check4">Total Row</label></td>
            <td>
                <input type="checkbox" id="Check5" /><label for="Check5">Last Column</label></td>
        </tr>
    </table>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#Ribbon"), {
                width: "600",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbon"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "Font",
                        content: [{
                            groups: [{
                                id: "fontColor",
                                toolTip: "Font Color",
                                contentID: "fontColor"
                            }],
                            // defaults settings to controls
                            defaults: {
                                height: 30,
                                type: ej.Ribbon.type.custom
                            }
                        }]
                    }, {
                        text: "Operators",
                        content: [{
                            groups: [{
                                id: "design",
                                type: ej.Ribbon.type.custom,
                                contentID: "design"
                            }]
                        }]
                    }]
                }],
                // event of Ribbon create to initialize custom control
                create: "createControl"
            });
        });
    }  
        function createControl(args) {
            var ribbon = $("#Ribbon").data("ejRibbon");
            $("#fontColor").ejColorPicker({ value: "#FFFF00", modelType: "palette", cssClass: "e-ribbon", toolIcon: "e-fontcoloricon" });
        }

{% endhighlight %}

![](Controls-Support_images/Controls-Support_img2.png)