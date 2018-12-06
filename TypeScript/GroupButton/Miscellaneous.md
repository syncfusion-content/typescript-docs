---
layout: post
title: Miscellaneous | GroupButton | TypeScript | Syncfusion
description: miscellaneous
platform: TypeScript
control: GroupButton
documentation: ug
---

# Miscellaneous

## Show/Hide the items

Particular currently showing button items can be hidden. Also it provides the options to show the hidden button again. These functionalities can be achieved using **showItem** or **hideItem** method.

**Hide the Button item based on given index**

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.hideItem(1);
    });
}

{% endhighlight %}

**Show the hidden Button item based on given index**

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.showItem(1);
    });
}

{% endhighlight %}

Also entire group button, can be hide/show using public methods hide(), show().

## Enable/Disable

Particular Items can be enabled/disabled using **enableItem**, **disableItem** methods. This takes the index of the button as the argument. 

Also entire GroupButton can be enabled or disabled using enable (), disable public method.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.disableItem(1);
    });
}

{% endhighlight %}

![Enable/Disable](Miscellaneous_images/Miscellaneous_img1.jpeg)


## Getting Index of given Element

By passing the jQuery element of the required button to **getIndex** public method, we can get the index of that passed button element.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.getIndex(id);
    });
}

{% endhighlight %}

## Getting state of given Button

You can get the selection state of required button by passing that button jQuery element to **isSelected** public method.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.selectItem(1);
        alert(groupButton.isSelected(1));
    });
}

{% endhighlight %}

Also you can get the active / disabled state required button by passing that button jQuery element to **isDisabled** public method.

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {
        });
        groupButton.disableItem(1);
        alert(groupButton.isDisabled(1));
    });
}

{% endhighlight %}

