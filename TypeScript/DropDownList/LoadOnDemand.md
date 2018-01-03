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

Load on demand feature allows the DropDownList items load on request from the service/database, during only on click the DropDown icon or DropDownList. This functionality helps to improve performance on control initial rendering time. Because data items load on request. 

The loadOnDemand property is used to enable or disable the load on demand functionality of the DropDownList.

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