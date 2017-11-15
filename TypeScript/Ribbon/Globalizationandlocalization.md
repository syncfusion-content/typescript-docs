---
layout: post
title: Globalization and Localization with Ribbon widget for Syncfusion Essential JS
description: How to use globalization and localization 
platform: Typescript
control: Ribbon
documentation: ug
---
# Globalization and Localization

## Localization

The localization support allows to customize the display of text within the Ribbon in a user-specific culture and locale. The Ribbon control can be localized in specific culture using the common API [`locale`](https://help.syncfusion.com/api/js/ejribbon#members:locale) along with the collection of localized words defined for that culture using the ej.Ribbon.Locale [culture-code].Please find the table with list of properties and its value in locale object.

<table>
<tr>
<th>
Locale key words </th><th>
Text</th></tr>
<tr>
<td>
CustomizeQuickAccess</td><td>
Customize Quick Access Toolbar</td></tr>
<tr>
<td>
RemoveFromQuickAccessToolbar</td><td>
Remove from Quick Access Toolbar</td></tr>
<tr>
<td>
AddToQuickAccessToolbar</td><td>
Add to Quick Access Toolbar</td></tr>
<tr>
<td>
ShowAboveTheRibbon</td><td>
Show Above the Ribbon</td></tr>
<tr>
<td>
ShowBelowTheRibbon</td><td>
Show Below the Ribbon</td></tr>
<tr>
<td>
MoreCommands</td><td>
More Commands...</td></tr>
</table>

N> By default, the Ribbon control is localized in `en-US` culture.

For further information on – how to refer the required culture scripts into your application, refer [`here`](https://help.syncfusion.com/js/localization).

{% highlight html %}

    <div id="defaultRibbon"></div>
              <ul id="ribbon">
                <li><a>FILE</a>
                 <ul>
                 <li><a>New</a></li>
                 </ul>
               </li>
            </ul>
          </div>
    <script>
	ej.Ribbon.Locale["es-ES"] = {
		CustomizeQuickAccess: "Agordu Rapida Aliro",
		RemovefromQuickAccessToolbar: "Forigu de Rapida Aliro Ilobreto",
		AddtoQuickAccessToolbar: "Aldoni al Rapida Aliro Ilobreto",
		ShowAbovetheRibbon: "Montru Super la Ribbona",
		ShowBelowtheRibbon: "Montru Sube la Ribbon",
		MoreCommands: "pli Komando"
	};
	$(function() {
		$("#defaultRibbon").ejRibbon({
			width: "600",
			locale: "es-ES",
			showQAT: true,
			applicationTab: {
				type: ej.Ribbon.applicationTabType.menu,
				menuItemID: "ribbon",
				menuSettings: {
					openOnClick: false
				}
			},
			tabs: [{
				id: "home",
				text: "HOME",
				groups: [{
					text: "Clipboard",
					alignType: ej.Ribbon.alignType.columns,
					content: [{
						groups: [{
							id: "paste",
							text: "paste",
							toolTip: "Paste",
							quickAccessMode: ej.Ribbon.quickAccessMode.toolBar,
							splitButtonSettings: {
								contentType: ej.ContentType.ImageOnly,
								prefixIcon: "e-icon e-ribbon e-ribbonpaste",
								targetID: "pasteSplit",
								buttonMode: "dropdown",
								arrowPosition: ej.ArrowPosition.Bottom,
								click: "executeAction"
							}
						}],
						defaults: {
							type: ej.Ribbon.type.splitButton,
							width: 50,
							height: 70
						}
					}]
				}]
			}]
		});
	});
	</script>

{% endhighlight %}

![](Globalizationandlocalization_images/Globalizationandlocalization._img1.png)

## Right to Left - RTL

By default, Ribbon render its content and layout from left to right. To customize Ribbon direction, you can change direction from LTR to RTL by using [`enableRTL`](https://help.syncfusion.com/api/js/ejribbon#members:enablertl) as true.

{% highlight html %}

    <div id="defaultRibbon"></div>
    <ul id="ribbon">
    <li>
        <a>FILE</a>
        <ul>
            <li><a>New</a></li>
            <li><a>Open</a></li>
            <li><a>Save</a></li>
        </ul>
    </li>
    </ul>
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#defaultRibbon"), {
            width: "40%",
            enableRTL: true,
            applicationTab: { type: ej.Ribbon.ApplicationTabType.Menu, menuItemID: "ribbon", menuSettings: { openOnClick: false } },
            tabs: [{
                id: "home", text: "HOME", groups: [{
                    text: "New", alignType: ej.Ribbon.AlignType.Rows, content: [{
                        groups: [{
                            id: "new",
                            text: "New",
                            toolTip: "New",
                            buttonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                imagePosition: ej.ImagePosition.ImageTop,
                                prefixIcon: "e-icon e-ribbon e-new",
                                click: "executeAction"
                            }
                        }
                        ],
                        defaults: {
                            type: ej.Ribbon.Type.Button,
                            width: 60,
                            height: 70
                        }
                    }]
                },
                {
                    text: "Clipboard", alignType: ej.Ribbon.AlignType.Columns, content: [{
                        groups: [{
                            id: "paste",
                            text: "paste",
                            toolTip: "Paste",
                            splitButtonSettings: {
                                contentType: ej.ContentType.ImageOnly,
                                prefixIcon: "e-icon e-ribbon e-ribbonpaste",
                                targetID: "pasteSplit",
                                buttonMode: "dropdown",
                                arrowPosition: ej.ArrowPosition.Bottom,
                                click: "executeAction"
                            }
                        }
                        ],
                        defaults: {
                            type: ej.Ribbon.Type.SplitButton,
                            width: 50,
                            height: 70
                        }
                    },
                    ]
                },
                ]
            },
            ]
        });
    });
}

{% endhighlight %}

![](Globalizationandlocalization_images/Globalizationandlocalization._img2.png)


