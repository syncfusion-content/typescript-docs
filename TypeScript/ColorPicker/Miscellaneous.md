---
layout: post
title: Miscellaneous
description: miscellaneous
platform: TypeScript
control: ColorPicker
documentation: ug
---

# Miscellaneous

## getValue

The **getValue**() method in **ColorPicker** returns the hexadecimal value.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ColorPickerComponent {
    $(function () {
      var ColorObj;
        var colorSample = new ej.ColorPicker($("#colorpick"), {
        ColorObj = $("#colorPicker").ejColorPicker({ value: "#278787" }).data('ejColorPicker');
        ColorObj.getValue();
    });
    });
}

{% endhighlight %}


## setValue

The **setValue**() method in **ColorPicker** is used to set the color value. The given value is in hexadecimal form.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}
  $(function () {

        var colorSample = new ej.ColorPicker($("#colorpick"), {

             })
        colorSample.setValue("#278787");
    });

{% endhighlight %}


## getColor

The **getColor**() method in **ColorPicker** control returns the color value in r,g,b,a form.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
  $(function () {

        var colorSample = new ej.ColorPicker($("#colorpick"), {
                  value: "#278787" 
        })
        colorSample.getColor();
    });

{% endhighlight %}