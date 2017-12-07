---
layout: post
title: Data-Binding
description: data binding
platform: typescript
control: BulletGraph	
documentation: ug

---

# Data Binding

**Bullet Graph** supports binding JSON data from a remote server or data created in client-side. You can use the **fields** property to customize the data bound with **Bullet Graph**.

## Local Data

Data available in client-side (local data) can be bound with **Bullet Graph** using **fields** property. This property provides option to specify data source, fields representing progress measure bar value, comparative measure value and category value.

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module BulletgraphComponent {

var localData = [
               {
                   value: 9.5, comparativeMeasureValue: 7.5,
                   category: 2001
               },
               {
                   value: 9.5, comparativeMeasureValue: 5,
                   category: 2002
               }]

    $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{
          qualitativeRangeSize: 60,
                    quantitativeScaleSettings: {
                        location: { x:50, y:20 },
                    },
                    height: 120,
                    fields: {
                        dataSource: localData, category: "category",
                        featureMeasures: "value",
                        comparativeMeasure: "comparativeMeasureValue"
                    }
        });
    });
}

{% endhighlight %}



The following screenshot displays **Bullet Graph** with local data generated using TypeScript

![](Data-Binding_images/Data-Binding_img1.png) 

## Remote Data

**Bullet Graph** provides option to bind data from a remote server using **ejDataManager** as data source in **fields** property. A query object should also be passed to **query** property when using data manager as data source.

{% highlight javascript %}

               //Creating data manager instance
                var dataManger = new ej.DataManager({
                    url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });

                // Query creation
                var query = ej.Query().from("Order_Details").take(3).where("UnitPrice", ej.FilterOperators.greaterThan, 18, false)
                    .where("UnitPrice", ej.FilterOperators.lessThanOrEqual, 40, false)
                    .where("Quantity", ej.FilterOperators.greaterThan, 5, false)
                    .where("Quantity", ej.FilterOperators.lessThanOrEqual, 45, false);

        $(function () {
        var sample = new ej.datavisualization.BulletGraph($("#BulletGraph"),{                                             fields: {
                        dataSource: dataManger,
                        query: query,
                        category: "ProductID",
                        featureMeasures: "UnitPrice",
                        comparativeMeasure: "Quantity"
                    },

                    qualitativeRanges: [{ rangeEnd: 25 }, { rangeEnd: 37 }, { rangeEnd: 45 }],

                    qualitativeRangeSize: 60,
                    quantitativeScaleSettings: {
                        location: { x: 50, y: 20 },
                        minimum: 5,
                        maximum: 45,
                        interval: 10,
                    },

                });
        });

{% endhighlight %}



The following screenshot displays a Bullet Graph bounded with data from a remote server

![](Data-Binding_images/Data-Binding_img2.png) 

