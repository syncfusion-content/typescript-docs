---
layout: post
title: Add-Group-Tiles
description: add group tiles
platform: typescript
control: Tile
documentation: ug
---

# Add Group Tiles

To make a **Tile** as grouped tile, you can use the following mentioned pre-defined classes.

<table>
<tr>
<th>
Class Name</th><th>
Explanation</th></tr>
<tr>
<td>
group</td><td>
To group the column elements</td></tr>
<tr>
<td>
column</td><td>
To align the tile in column manner</td></tr>
<tr>
<td>
small-col-2</td><td>
To align the small size tiles</td></tr>
</table>

To render group tile, refer to the following code example.

{% highlight html %}

    <div class="**group**">
        <div class="**column**">
               <!— Add tile control here -->
        </div>
    </div>

{% endhighlight %}

To render **column** grouped tile, you need to render the number of tiles inside a **&lt;div&gt;** element with class ‘**column’**. Then that column group element is appended to a **&lt;div&gt;** with class ‘**group’**.     

To render **small-col-2** grouped tile, you need to render the number of tiles inside a **&lt;div&gt;** element with class ‘**small-col-2**’. Then that **small-col-2** group element is appended to a **&lt;div&gt;** with class ‘**column’**. Then you need to append those column inside the main group **&lt;div&gt;** element.                                                     

 Refer the following code examples.

{% highlight html %}
    
    <div class="group">
            <div class="column">
                <div id="tile1">
                </div>
                <div id="tile2">
                </div>
                <div id="tile3">
                </div>
                <div id="tile4">
                </div>
                <div id="tile5">
                </div>
            </div>
            <div class="column">
                <div id="tile6">
                </div>
                <div id="tile7">
                </div>
                <div id="tile8">
                </div>
                <div id="tile9">
                </div>
                <div id="tile10">
                </div>
                <div id="tile11">
                </div>
            </div>
        </div>

{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}  
       
/// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />

module TileViewComponent {
    $(function () {
        var tile1 = new ej.Tile($("#tile1"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/alerts.png",
            text: "Alerts"
        });
       var tile2 = new ej.Tile($("#tile2"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/pictures.png",
            text: "Pictures"
        });
        var tile3 = new ej.Tile($("#tile3"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/camera.png",
            text: "Camera"
        });
       var tile4 = new ej.Tile($("#tile4"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/messages.png",
            text: "Messages"
        });
        var tile5 = new ej.Tile($("#tile5"), {
            tileSize: "wide", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/games.png",
            text: "Games"
        });
        var tile6 = new ej.Tile($("#tile6"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/map.png",
            text: "Map"
        });
       var tile7 = new ej.Tile($("#tile7"), {	 
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/bing.png",
            text: "Bing"
        });
       var tile8 = new ej.Tile($("#tile8"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/favs.png",
            text: "Health"
        });
        var tile9 = new ej.Tile($("#tile9"), {
            tileSize: "medium", imagePosition: "fill",
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/people_2.png",
            text: "Peoples"
        });
        var tile9 = new ej.Tile($("#tile10"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/weather.png",
            text: "Weather"
        });
       var tile9 = new ej.Tile($("#tile11"), {
            tileSize: "medium", 
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/music.png",
            text: "Music"
        });
    });
}

{% endhighlight %}



![](Add-Group-Tiles_images/Add-Group-Tiles_img1.png)

