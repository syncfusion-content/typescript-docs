---
layout: post
title: state persistence
description: state persistence
platform: typescript
control: DateRangePicker
documentation: ug 
---

## State Persistence

The value of DateRangePicker can be sustained even after form post back and page refreshing by enabling the **enablePersistence** API like below code example.
{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DateRangePickerComponent {
    $(function () {
        var datetimeSample = new ej.DateRangePicker($("#daterangepick"), {
                 enablePersistence: true
        });
    });
}
{% endhighlight %}
The DateRangePicker Model value will be stored in local storage / cookies of browser before page refreshes and reinitialized with the restored model after refresh.