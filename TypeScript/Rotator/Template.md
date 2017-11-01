---
layout: post
title: Template
description: template 
platform: typescript
control: Rotator
documentation: ug
---

# Template 

The Rotator widget’s appearance can be customized based on different needs using templates. The desired templates can be defined using the “template” property.

You can refer the following code example of template in Rotator.


  {% highlight html %}
  
            <div class="cols-sample-area">
                <div class="frame">
                    <ul id="sliderContent">
                    </ul>
                </div>
            </div>


  {% endhighlight %}

  {% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module RotatorComponent {
    $(function () {
		    var themesList = [
				{ text: "Colorful-Night", url: "../content/images/rotator/snowfall.jpg" },
				{ text: "Technology", url: "../content/images/rotator/tablet.jpg" },
				{ text: "Nature", url: "../content/images/rotator/nature.jpg" },
				{ text: "Snow Fall", url: "../content/images/rotator/snowfall.jpg" },
				{ text: "Credit Card", url: "../content/images/rotator/card.jpg" },
				{ text: "Beautiful Bird", url: "../content/images/rotator/bird.jpg" },
				{ text: "Amazing Sculptures", url: "../content/images/rotator/sculpture.jpg" }				
				];

      var rotatorInstance = new ej.Rotator($("#sliderContent"), {
			    dataSource: themesList,
          slideWidth: "100%",
          frameSpace: "0px",
				  slideHeight: "auto",
				  template: '<div class="image"><img src = ${url} title = ${text} class="image"/> </div>' 				
        });
    });
}

  {% endhighlight %}


