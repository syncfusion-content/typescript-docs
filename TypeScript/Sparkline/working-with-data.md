---
layout: post
title: Data binding
description: Learn how to bind Sparkline with local data.
platform: ts
control: Sparkline
documentation: ug

---

# Working with Data

## Local Data

1. You can bind the data to the Sparkline by using `dataSource`property and then you need to map the **X** and **Y** value with `xName` and `yName` properties respectively.

{% highlight javascript %}

var sparkLineData = [
{ employeeId: 1, sales: 25 },
{ employeeId: 2, sales: 28 },
{ employeeId: 3, sales: 34 },
{ employeeId: 4, sales: 32 },
{ employeeId: 5, sales: 40 },
{ employeeId: 6, sales: 32 },
{ employeeId: 7, sales: 35 },
{ employeeId: 8, sales: 55 },
{ employeeId: 9, sales: 38 },
{ employeeId: 10, sales: 30 }];
    
module linesparkline {
    $(function () {
         //..//
        var sample = new ej.Sparkline($("#line"), {
     dataSource: sparkLineData,
     xName: "employeeId",
     yName: "sales",
     //..//
});
    });
}


{% endhighlight %}


![](Working-with-Data_images/Working-with-Data_img1.png); 

2. You can also bind an array of data to Sparkline by using `dataSource` property.  

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module linesparkline {
    $(function () {
         //..//
        var sample = new ej.Sparkline($("#line"), {
            dataSource: [12, 14, 11, 12, 11, 15, 12, 10, 11, 12, 15, 13, 12, 11, 10, 13, 15, 12, 14, 16, 14, 12, 11],
            //..//
        });
    });
}

{% endhighlight %}

![](Working-with-Data_images/Working-with-Data_img2.png); 


