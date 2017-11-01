---
layout: post
title: Data-Binding
description: data binding
platform: typescript
control: Rotator
documentation: ug
---

# Data Binding

**Rotator** provides a flexible approach for binding the data from various data sources. There are various properties in **Toolbar** for **Data Binding**. The value set to this property is **object** type.

## Data fields and Configuration

The following sub-properties provide a way to bind the data either locally/remotely to the **Rotator** control. The value set to this property is **object** type.

## DataSource

This property specifies the list of data that contains a set of data fields. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Fields

It defines mapping fields for the data items of the **Rotator**. The value set to this property is **object** type.

## Text

It specifies the text content of the tag. The value set to this property is **string** type.

## URL

This property specifies the **URL** for an image. The value set to this property is **string** type.

## Query

This property retrieves data from remote data. This property is applicable only when a remote data source is used. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Local data binding

**Rotator** provides the data binding support for the **Rotator** **item**. So you can bind the data from **JSON** **Data**. For this behavior, you need to map the corresponding filed with their column names. The data can be bound as a list and it is assigned to **dataSource** property. You can refer the following code example to bind local data.

  {% highlight html %}

<div class="cols-sample-area">
  <ul id="sliderContent"></ul>
</div>

  {% endhighlight %}


  {% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var website = [
      { text: "Beautiful Bird", url: "../images/rotator/bird.jpg" },
      { text: "Colorful Night", url: "../images/rotator/night.jpg" },
      { text: "Technology", url: "../images/rotator/tablet.jpg" },
      { text: "Nature", url: "../images/rotator/nature.jpg" },
      { text: "Snow Fall", url: "../images/rotator/snowfall.jpg" },
      { text: "Credit Card", url: "../images/rotator/card.jpg" },
      { text: "Amazing Sculptures", url: "../images/rotator/sculpture.jpg" }
        ];
     var rotatorInstance = new ej.Rotator($("#sliderContent"), {
            slideWidth: "600px",
            frameSpace: "0px",
            displayItemsCount: "1",
            slideHeight: "350px",
            navigateSteps: "1",
            enableResize: true,
            pagerPosition: ej.Rotator.PagerPosition.Outside,
            dataSource: website,
            orientation: ej.Orientation.Horizontal,
            showPager: true,
            enabled: true,
            showCaption: true,
            allowKeyboardNavigation: true,
            enableRTL: true,
            showPlayButton: true,
            animationType: "slide"
        });
    });
}
  {% endhighlight %}


![](Data-Binding_images/Data-Binding_img1.png)

