---

layout: post
title: Load on demand in DropDownList widget 
description: Describes about the load on demand in DropDownList widget 
platform: Typescript
control: DropDownList
documentation: ug
keywords: DropDownList, loadOnDemand
---

## Load On Demand

The popup and lists will be generated while click on dropdown icon or text box. For this feature, the loadOnDemand property must be enabled.

{% highlight html %}

    <input type="text" id="bikeList" />
   
{% endhighlight %}

{% highlight javascript %}

module DropDownListComponent {
    var BikeList = [
        { empid: "bk1", text: "Apache RTR" }, { empid: "bk2", text: "CBR 150-R" }, { empid: "bk3", text: "CBZ Xtreme" },
        { empid: "bk4", text: "Discover" }, { empid: "bk5", text: "Dazzler" }, { empid: "bk6", text: "Flame" },
        { empid: "bk7", text: "Fazzer" }, { empid: "bk8", text: "FZ-S" }, { empid: "bk9", text: "Pulsar" },
        { empid: "bk10", text: "Shine" }, { empid: "bk11", text: "R15" }, { empid: "bk12", text: "Unicorn" }
    ];
    $(function () {
        var sample = new ej.DropDownList($("#bikeList"),{
            dataSource: BikeList,
            width: "100%",
            watermarkText: "Select a bike",
            fields: { id: "empid", text: "text", value: "text" },
            loadOnDemand: true,  
            showRoundedCorner: true
        });
    });

}
       

{% endhighlight %}

![](LoadOnDemand/loadondemand.png)