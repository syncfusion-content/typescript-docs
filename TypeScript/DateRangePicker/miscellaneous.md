---
layout: post
title: miscellaneous 
description: miscellaneous 
platform: typescript
control: DateRangePicker
documentation: ug
---

## Miscellaneous 

### Enable / Disable

The control can be enabled / disabled using public methods, **enable** or **disable**. 

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {"disable"});
    });
}

{% endhighlight %}


{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {"enable"});
    });
}

{% endhighlight %}


### Allow Editing

Editing in input box can be disabled by setting the false value to **allowEdit** API. By default this will be false and we can edit the value in input box

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {

            allowEdit: false

        });
    });
}    
        
{% endhighlight %}


### Clear ranges

To clear the all selection and ranges in a popup we can make use of **clearRanges** method.

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {"clearRanges"});
    });
}

{% endhighlight %}

