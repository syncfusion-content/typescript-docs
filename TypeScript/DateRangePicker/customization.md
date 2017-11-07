---
layout: post
title: customization
description: customization
platform: typescript
control: DateRangePicker
documentation: ug
---

## Customization

With available flexible options customization of DateRangePicker will be easier.

### Setting Dimension

**Height** and **width** of the DateRangePicker can be changed using corresponding API (**height,width**) like below code examples.

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {

        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {

            height: 50,

            width: 300

        });
    });
}

{% endhighlight %}

### Rounded Corners

You can make use of **showRoundedCorner** property in order to add rounded borders to the input and popup elements. By default, in DateRangePicker this will be disabled state we can enable this by setting true to this API.

// creates DateRangePicker and setting rounded corner dynamically


{% highlight html %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {

                        showRoundedCorner: true
        });
    });
 }

{% endhighlight %}