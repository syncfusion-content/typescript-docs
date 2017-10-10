---
title: Schedule - Context Menu	
description: Default and Custom context menu options for appointments and cells in Scheduler
platform: typescript
control: schedule
documentation: ug
keywords: context-menu
---
# Context Menu

Scheduler provides default context menu options for both appointments as well as work cells. It also allows to define additional custom context menu options.

The options that are available under [contextMenuSettings](/api/js/ejschedule#members:contextmenusettings) are as follows,

* **enable** - Enables/disables the context menu option in Scheduler.
* **menuItems** - Contains the sub-menu collections related to both the appointment and cells.

## Default Menu Options

The menu items contains two separate collection based on the appointment and cells.

### Appointment

The appointment collection includes the following options.

<table>
    <tr>
        <td>Open Appointment (default)</td>
    </tr>
    <tr>
        <td>Delete Appointment (default)</td>
    </tr>
    <tr>
        <td>Print Appointment</td>
    </tr>
    <tr>
        <td>Categorize</td>
    </tr>
</table>

### Cells

The default options available within the cell collection includes -

<table>
    <tr>
        <td>New Appointment</td>
    </tr>
    <tr>
        <td>New Recurring Appointment</td>
    </tr>
    <tr>
        <td>Today</td>
    </tr>
    <tr>
        <td>Go to date</td>
    </tr>
    <tr>
        <td>Settings (View, TimeMode, Work Hours) </td>
    </tr>
</table>

The following code snippet shows how to enable the context menu settings in Scheduler and to make use of it with default available options.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [
                        { id: "open", text: "Open Appointment" },
                        { id: "delete", text: "Delete Appointment" }
                    ],
                    cells: [
                        { id: "new", text: "New Appointment" },
                        { id: "recurrence", text: "New Recurring Appointment" },
                        { id: "today", text: "Today" },
                        { id: "goToDate", text: "Go to date" },
                        { id: "settings", text: "Settings" },
                        { id: "view", text: "View", parentId: "settings" },
                        { id: "timeMode", text: "TimeMode", parentId: "settings" },
                        { id: "view_Day", text: "Day", parentId: "view" },
                        { id: "view_Week", text: "Week", parentId: "view" },
                        { id: "view_Workweek", text: "Workweek", parentId: "view" },
                        { id: "view_Month", text: "Month", parentId: "view" },
                        { id: "timeMode_Hour12", text: "12 Hours", parentId: "timeMode" },
                        { id: "timeMode_Hour24", text: "24 Hours", parentId: "timeMode" },
                        { id: "workhours", text: "Work Hours", parentId: "settings" }
                    ]
                }
            },
            appointmentSettings: {
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30)
                }]
            }
        });
    });
}

{% endhighlight %}

N> In agenda view, only the appointment menu items shows up in the context menu options. For default menu items, the id must be defined the same as mentioned in the above code example – as we have processed the menus based on this id within our source.

## Custom Menu Options

Apart from the default available options, it is also possible to add custom menu options to the context-menu of both the appointment and cell collection.

The following code example depicts how **to add the custom menu items** to the appointment and cell collection of the context menu settings.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [
                        { id: "open", text: "Open Appointment" },
                        { id: "delete", text: "Delete Appointment" },
                        { id: "option1", text: "User Option 1" }
                    ],
                    cells: [{
                        id: "celloption1",
                        text: "Custom Option 1"
                    }]
                }
            },
            appointmentSettings: {
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30)
                }]
            }
        });
    });
}

{% endhighlight %}

N> The **id** given for the custom menu items **must be unique** in both the appointment and cell collection.

## Handling Menu Actions

To define specific actions for a click made on the custom menu items, the client-side event [menuItemClick](/api/js/ejschedule#events:menuitemclick) can be used as depicted in the below code example.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [
                        { id: "open", text: "Open Appointment" },
                        { id: "delete", text: "Delete Appointment" },
                        { id: "option1", text: "User Option 1" }
                    ]
                }
            },
            appointmentSettings: {
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30)
                }]
            },
            menuItemClick: "onMenuItemClick"
        });
    });
}

{% endhighlight %}

{% highlight javascript %}

function onMenuItemClick(args) {
    //args.events contains information of the clicked menu item.
    if (args.events.ID == "option1")
        alert("Custom menu clicked");
}

{% endhighlight %}

Also, it is possible to predict the target on which the right click is made, either on the cells or appointments with the use of the event [beforeContextMenuOpen](/api/js/ejschedule#events:beforecontextmenuopen). The below code example shows how to block the display of context menu, when right clicked on the cells by setting **args.cancel** as **true**.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [{
                        id: "open",
                        text: "Open Appointment"
                    }, {
                        id: "delete",
                        text: "Delete Appointment"
                    }, {
                        id: "option1",
                        text: "User Option 1"
                    }]
                }
            },
            appointmentSettings: {
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30)
                }]
            }
            beforeContextMenuOpen: "onBeforeContextMenuOpen"
        });
    });
}

{% endhighlight %}

{% highlight javascript %}

function onBeforeContextMenuOpen(args) {
    //args.events.target – target information to depict either cell/appointment
    if ($(args.events.target).hasClass("e-workcells") || $(args.events.target).hasClass("e-monthcells"))
        args.cancel = true;
}

{% endhighlight %}

## Adding Categorize Option

To include the default categorize option within the context menu, it is necessary to enable the [categorizeSettings](/api/js/ejschedule#members:categorizesettings) property as shown in the below code example.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [{
                        id: "open",
                        text: "Open Appointment"
                    }, {
                        id: "delete",
                        text: "Delete Appointment"
                    }, {
                        id: "categorize",
                        text: "Categorize"
                    }]
                }
            },
            categorizeSettings: {
                enable: true
            },
            appointmentSettings: {
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30)
                }]
            }
        });
    });
}

{% endhighlight %}

N> The **categorize** option must be added only to the **appointment** collection, which displays on right clicking the appointments.

## Remote Data Binding for Categorize

In Schedule, we can also binding the categorize datasource using remote data. The below code example shows how to bind the datasource to categorizeSettings.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ScheduleComponent {
    $(function () {
        var dataManager = ej.DataManager({
            url: "Home/GetCategorizeData",
            adaptor: new ej.UrlAdaptor()
        });
        var sample = new ej.Schedule($("#Schedule1"), {
            currentDate: new Date(2015, 11, 2),
            categorizeSettings: {
                enable: true,
                allowMultiple: true,
                dataSource: dataManager,
                id: "Id",
                fontColor: "FontColor",
                color: "Color",
                text: "Text"
            },
            appointmentSettings: {
                categorize: "Categorize",
                dataSource: [{
                    Id: 100,
                    Subject: "Research on Sky Miracles",
                    StartTime: new Date(2015, 11, 2, 9, 00),
                    EndTime: new Date(2015, 11, 2, 10, 30),
                    Categorize: "1"
                }]
            }
        });
    });
}

{% endhighlight %}

The server-side controller code to handle the CRUD operations are as follows.

{% highlight c# %}

public JsonResult GetCategorizeData()
{
    // ScheduleDataDataContext is a LINQ-to-SQL data class name that is defined in the .dbml file to access the tables from the database
    IEnumerable data = new ScheduleDataDataContext().CategoryData;
    return Json(data, JsonRequestBehavior.AllowGet);
}

{% endhighlight %}
