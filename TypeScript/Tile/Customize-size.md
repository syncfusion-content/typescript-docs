---
layout: post
title: Customize-size
description: customize size
platform: typescript
control: Tile
documentation: ug
---

# Customize size

You can customize the size of the **Tile** by using **“data-ej-tileSize”** attribute. The following built-in tile sizes are supported.

1. medium
2. small
3. large
4. wide

The default **TileSize** value is set to **small**.

Refer to the following code examples.

{% highlight html %}
    
    <div id="tile"></div>
    
{% endhighlight %}   

Add the following code inside the **script** tag.

{% highlight javascript %}
    
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TileViewComponent {
    $(function () {
        var tile1 = new ej.Tile($("#tile1"), {
            tileSize: "medium", imagePosition: "center",
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/pictures.png",
            text: "Pictures"
        });
    });
}

{% endhighlight %}



![](Customize-size_images/Customize-size_img1.png)

