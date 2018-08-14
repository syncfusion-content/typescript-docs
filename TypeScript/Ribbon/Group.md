---
layout: post
title:  Group
description: group
documentation: ug
platform: Typescript
keywords: group,ribbon group
---

# Group

[`Group`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups) is a collection of logical content groups that are combined under related Tab. Each group can be defined using content groups or custom content.

## Adding Tab Groups

Group items can be added to Tabs by specifying [`text`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-text) and corresponding [`content`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content) to be displayed. The content of group can be specified as either with [`content`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content) collection, [`contentID`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-contentid) or [`customContent`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-customcontent). You can add tab group dynamically in the ribbon control with given tab index, tab group object and group index position by using [`addTabGroup`](https://help.syncfusion.com/api/js/ejribbon#methods:addtabgroup) method.

### Adding Content

Add content to Group item which is based on [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-type) of content specified. The available types are `button`, `splitButton`, `toggleButton`,`gallery`, and `dropDownList`.

Groups and defaults settings can be added with the [`content`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content). You can add group content dynamically in the ribbon control with given tab index, group index, content, content index and sub group index position by using [`addTabGroupContent`](https://help.syncfusion.com/api/js/ejribbon#methods:addtabgroupcontent).

#### _Defaults_

The [`tabs.groups.content.defaults.height`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults-height), [`tabs.groups.content.defaults.width`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults-width), 
[`tabs.groups.content.defaults.type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults-type), [`tabs.groups.content.defaults.isBig`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults-isbig) property to the controls in the [`group`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups) can be specified commonly.

The `height` & `width` applicable to button, split button, dropdown list ,Toggle button controls and `isBig` applicable to only button controls ( button, split , toggle)

#### _Adding Content Groups_

Controls such as button, split button, dropdown list, toggle button, gallery in the subgroup of the Ribbon tab can be rendered. All of these can be customized using its corresponding settings property such as [`buttonSettings`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-buttonsettings), `dropdownSettings`, etc.

Custom controls or items (such as table, div etc.) can be added when the [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-type) set as `custom`. [`defaults`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-defaults) control settings of group can be specified for an `individual group` instead of specifying them to groups collection commonly.

[`Tooltip`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-tooltip) and [`Custom Tooltip`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-customtooltip) can be specified for each group controls.

{% highlight html %}
	
	<div id="Ribbon"></div>
	<ul id="ribbon">
		<li>
			<a>FILE</a>
			<ul>
				<li><a>Open</a></li>
			</ul>
		</li>
	</ul>
	<ul id="pasteSplit">
		<li>Paste
		</li>
		<li>Paste Special
		</li>
	</ul>

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
				//tab collection
				tabs: [{
					id: "home",
					text: "HOME",
					//group collection of home tab
					groups: [{
						text: "ClipBoard",
						// content collection of group
						content: [{
							groups: [{
								// content group with splitbutton id , text & button settings
								id: "paste",
								text: "Paste",
								toolTip: "Paste",
								isBig: true,
								type: ej.Ribbon.type.splitButton,
								splitButtonSettings: {
									contentType: ej.ContentType.ImageOnly,
									prefixIcon: "e-icon e-ribbon e-ribbonpaste",
									targetID: "pasteSplit"
								}
							}]
						}]
					}, {
						text: "Font",
						//group align type as columns
						alignType: ej.Ribbon.alignType.columns,
						content: [{
							groups: [{
								// content group with toggle button settings
								id: "cut",
								toggleButtonSettings: {
									defaultText: "Cut",
									activeText: "Cut Over"
								}
							}, {
								id: "copy",
								toggleButtonSettings: {
									defaultText: "Copy",
									activeText: "Copy Over"
								}
							}],
							// defaults settings of above group’s control
	
							defaults: {
								width: 75,
								height: 30,
								type: ej.Ribbon.type.toggleButton
							}
						}],
					}]
				}]
			});
		});
}

{% endhighlight %}

![](Ribbon/Group_images/Group_img1.png)

#### _Enable Separator_ 

Separates the control from the next control in the group when group `alignType` is `row`. Set “true” to [`enableSeparator`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-content-groups-enableseparator).

{% highlight html %}

	<div id="Ribbon"></div>
    <ul id="ribbon">
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
                width: "500",
                applicationTab: {
                    type: ej.Ribbon.applicationTabType.menu,
                    menuItemID: "ribbon"
                },
                tabs: [{
                    id: "home",
                    text: "HOME",
                    groups: [{
                        text: "New",

                        // group alignType is "row”
                        alignType: ej.Ribbon.alignType.rows,
                        content: [{
                            groups: [{
                                id: "new",
                                text: "New",
                                toolTip: "New",

                                // separates New and Font controls
                                enableSeparator: true,
                                buttonSettings: {
                                    width: 100,
                                }
                            }, {
                                id: "font",
                                text: "Font",
                                toolTip: "Font",
                                buttonSettings: {
                                    width: 150,
                                }
                            }],
                            defaults: {
                                type: ej.Ribbon.type.button,
                                height: 70
                            }
                        }]
                    }]
                }]
            });
        });
 }


{% endhighlight %}

![](Group_images/Group_img2.png)

### Adding Custom Content 

Set group [`type`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-type) as `custom` to add custom items such as div, table and custom controls. With type as custom, content can be added in two ways as specified below.

*	HTML contents can be directly added into the groups as string content using [`customContent`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-customcontent) property
*	Custom template id can be specified to render those specific custom template using [`contentID`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-contentid) property

{% highlight html %}

	<div id="Ribbon"></div>
	<ul id="ribbon">
		<li><a>FILE </a>
			<ul>
				<li><a>New</a></li>
			</ul>
		</li>
	</ul>
	<button id="button">Using Content ID</button>

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
						text: "New",
						type: "custom",
						customContent: "<button id='customContent'>Using Custom Content</button>"
					}, {
						text: "Data",
						type: "custom",
						contentID: "button"
					}]
				}]
			});
		});
}

{% endhighlight %}

![](Group_images/Group_img3.png)

## Group Expander

Set [`enableGroupExpander`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-enablegroupexpander) as true to show Group Expander for each group in Tab. These expanders can be customized using [`groupExpand`](https://help.syncfusion.com/api/js/ejribbon#events:groupexpand) event, such as to show popup dialog. To specify tooltip for the group expander of the group [`tabs.groups.groupExpanderSettings`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-groupexpandersettings) and 
[`tabs.groups.groupExpanderSettings.toolTip`](https://help.syncfusion.com/api/js/ejribbon#members:tabs-groups-groupexpandersettings-tooltip) can be used.

{% highlight html %}

    <div id="Ribbon"></div>
    <ul id="ribbon">
        <li><a>FILE </a>
            <ul>
                <li><a>New</a></li>
            </ul>
        </li>
    </ul>    
    <button id="button">Home button</button>

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
                        text: "New",
                        alignType: ej.Ribbon.alignType.rows,
                        type: "custom",

                        // group expander enabled
                        enableGroupExpander: true,
                        contentID: "button"
                    }]
                }],

                // event of group expander
                groupExpand: function (args) {
                    alert("Group expander click triggered");
                }
            });
        });

}
{% endhighlight %}

![](Group_images/Group_img4.png)

