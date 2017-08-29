---
layout: post
title: State-Maintenance
description: state maintenance
platform: TypeScript
control: ProgressBar
documentation: ug
---

# State Maintenance

Save current model value to cookies for **State Maintenance**. While refreshing the ProgressBar widget, page retains the model value applied from browser cookies. By default, the ‘**enablePersistence**’ property is set to ‘**false**’ in the ProgressBar.

The following steps explain the **State Maintenance** in the ProgressBar control.

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}

<div class="control">
    <div id="progressbar"></div>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Add the following script to enable State Maintenance.
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ProgressBarComponent {
    $(function () {
        var sample = new ej.ProgressBar($("#progressbar"),{
            enablePersistence: true,
            value: 40,
            width: 500,
            height: 40
        });
        sample.setModel({ text: progress.getValue() + " %" });
    });
}

{% endhighlight %}

The following screenshot displays the output.

![](State-Maintenance_images/State-Maintenance_img1.png) 

