---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: typescript
control: Rotator
documentation: ug
---

# Appearance and Styling

## Adjusting rotator item size

### Slide width

This property sets the **width** of a **Rotator** Item. The value set to this property is **string** or **number**.


  {% highlight javascript %}
  
/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
          slideWidth: "500px"
          });
    });
}
  {% endhighlight %}
  
  
  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
          slideWidth: 500 
          });
    });
}
  {% endhighlight %}


### Slide height

This property sets the **height** of a **Rotator** Item. The value set to this property is **string** or **number**.


  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
           slideHeight: "500px"
         });
    });
  }  

  {% endhighlight %}
  
  
  {% highlight javascript %}
  	
/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module RotatorComponent {
    $(function () {
        var rotatorInstance = new ej.Rotator($("#sliderContent"), {
          slideHeight: 500 
        });
    });
}

  {% endhighlight %}

