---
layout: post
title:  onDemand
description: onDemand
documentation: ug
platform: Typescript
keywords: onDemand
---

# Load on Demand

Set [`enableOnDemand`](https://help.syncfusion.com/api/js/ejribbon#members:enableondemand) as true to enable load tab and backstage contents dynamically. Loading content on demand improves the initial rendering time of the ribbon by rendering tab and backstage content when tabs and backstage items are clicked.
 
{% highlight html %}

           <div id="defaultRibbon"></div>
               <div id="newCon">
                    <table>
                        <tr>
                            <td>
                                <button id="button" class="e-bsnewbtnstyle">Blank WorkBook</button>
                            </td>
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
                

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#defaultRibbon"), {
               width: "50%",
               enableOnDemand: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Backstage,
                    backstageSettings: {
                        text: "FILE",
                        height: 360,
                        width: 600,
                        headerWidth: 125,
                        pages: [{ id: "new", text: "New", contentID: "newCon" },
                                { id: "close", text: "Close", enableSeparator: true, itemType: ej.Ribbon.itemType.button },
                                { id: "account", text: "Office Account", contentID: "accountCon"}]
                    }
                },
                tabs: [{
                    id: "home", text: "HOME", groups: [{
                        text: "Clipboard", alignType: ej.Ribbon.AlignType.Columns, groupExpanderSettings: {
                            toolTip: "Clipboard"
                        }, content: [{
                            groups: [{
                                id: "paste",
                                text: "paste",
                                toolTip: "Paste",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-icon e-ribbon e-ribbonpaste"
                                }
                            }
                            ],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                isBig: true,
                                width: 50,
                                height: 70
                            }
                        }]
                    },
                  	{
					    text: "New", alignType: ej.Ribbon.AlignType.Rows, content: [{
					        groups: [{
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
					            type: ej.Ribbon.Type.Button,
					            width: 60,
					            height: 70
					        }
					    }]
					}]
                },
				{
				    id: "layout", text: "LAYOUT", groups: [{
				        text: "Alignment", alignType: ej.Ribbon.AlignType.Rows, content: [
						{
						    groups: [{
						        id: "bullet",
						        text: "Bullet Format",
						        toolTip: "Bullets",
						        buttonSettings: {
						            contentType: ej.ContentType.ImageOnly,
						            prefixIcon: "e-icon e-ribbon e-bullet"
						        }
						    },
                             {
                                 id: "number",
                                 text: "Number Format",
                                 toolTip: "Numbering",
                                 buttonSettings: {
                                     contentType: ej.ContentType.ImageOnly,
                                     prefixIcon: "e-icon e-ribbon e-numbericon"
                                 }
                             }],
						    defaults: {
						        type: ej.Ribbon.Type.Button,
						        isBig: false
						    }
						}]
				    }]
				}],
            });
        });
     var buttonsample = new ej.Button($("#button"), {
            size: "large",
            height: 200,
            width: 225,
            contentType: "textandimage",
            imagePosition: "imagetop",
            prefixIcon: "e-icon e-blank e-infopageicon"
        });
  }
     <style>
       .e-accuser {
           background-image: url("../content/ejthemes/common-images/ribbon/User.jpg"),url("content/ejthemes/common-images/ribbon/User.jpg");
        }
        .e-blank {
           background-image: url("../content/ejthemes/common-images/ribbon/blank.png"),url("content/ejthemes/common-images/ribbon/blank.png");
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

![](On_Demand_images/onDemand_img1.png)

# Initially Collapsible

Set [`collapsible'](https://help.syncfusion.com/api/js/ejribbon#members:collapsible) as true to render ribbon control in collapsed state, which results ribbon tabs to render without any content initially.
While using initially collapsible ribbon with [`enableOnDemand`](https://help.syncfusion.com/api/js/ejribbon#members:enableondemand) feature improves the performance by reducing initial loading time of ribbon.

{% highlight html %}

              <div id="defaultRibbon"></div>
                <div id="newCon">
                    <table>
                        <tr>
                            <td>
                                <button id="button" class="e-bsnewbtnstyle">Blank WorkBook</button>
                            </td>
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
                
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RibbonComponent {
    $(function () {
        var sample = new ej.Ribbon($("#defaultRibbon"), {
                width: "50%",
                enableOnDemand: true,
                collapsible: true,
                applicationTab: {
                    type: ej.Ribbon.ApplicationTabType.Backstage,
                    backstageSettings: {
                        text: "FILE",
                        height: 360,
                        width: 600,
                        headerWidth: 125,
                        pages: [{ id: "new", text: "New", contentID: "newCon" },
                                { id: "close", text: "Close", enableSeparator: true, itemType: ej.Ribbon.itemType.button },
                                { id: "account", text: "Office Account", contentID: "accountCon"}]
                    }
                },
                tabs: [{
                    id: "home", text: "HOME", groups: [{
                        text: "Clipboard", alignType: ej.Ribbon.AlignType.Columns, groupExpanderSettings: {
                            toolTip: "Clipboard"
                        }, content: [{
                            groups: [{
                                id: "paste",
                                text: "paste",
                                toolTip: "Paste",
                                buttonSettings: {
                                    contentType: ej.ContentType.ImageOnly,
                                    prefixIcon: "e-icon e-ribbon e-ribbonpaste"
                                }
                            }
                            ],
                            defaults: {
                                type: ej.Ribbon.Type.Button,
                                isBig: true,
                                width: 50,
                                height: 70
                            }
                        }]
                    },
                  	{
					    text: "New", alignType: ej.Ribbon.AlignType.Rows, content: [{
					        groups: [{
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
					            type: ej.Ribbon.Type.Button,
					            width: 60,
					            height: 70
					        }
					    }]
					}]
                },
				{
				    id: "layout", text: "LAYOUT", groups: [{
				        text: "Alignment", alignType: ej.Ribbon.AlignType.Rows, content: [
						{
						    groups: [{
						        id: "bullet",
						        text: "Bullet Format",
						        toolTip: "Bullets",
						        buttonSettings: {
						            contentType: ej.ContentType.ImageOnly,
						            prefixIcon: "e-icon e-ribbon e-bullet"
						        }
						    },
                             {
                                 id: "number",
                                 text: "Number Format",
                                 toolTip: "Numbering",
                                 buttonSettings: {
                                     contentType: ej.ContentType.ImageOnly,
                                     prefixIcon: "e-icon e-ribbon e-numbericon"
                                 }
                             }],
						    defaults: {
						        type: ej.Ribbon.Type.Button,
						        isBig: false
						    }
						}]
				    }]
				}],
            });
        });
    var buttonsample = new ej.Button($("#button"), {
            size: "large",
            height: 200,
            width: 225,
            contentType: "textandimage",
            imagePosition: "imagetop",
            prefixIcon: "e-icon e-blank e-infopageicon"
        });
 }
    
     <style>
       .e-accuser {
           background-image: url("../content/ejthemes/common-images/ribbon/User.jpg"),url("content/ejthemes/common-images/ribbon/User.jpg");
        }
        .e-blank {
           background-image: url("../content/ejthemes/common-images/ribbon/blank.png"),url("content/ejthemes/common-images/ribbon/blank.png");
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

![](On_Demand_images/onDemand_img2.png)