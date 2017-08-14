---
layout: post
title: Getting-Started
description: getting started
platform: typescript
control: Tile
documentation: ug
---

# Getting Started

This section helps you to understand the getting started of the Tile control with the step-by-step instructions.

## Create a Tile

The following steps guide you to add a Tile control.

1)	Refer the common Typescript [Getting Started Documentation](https://help.syncfusion.com/js/typescript) to create an application and add necessary scripts and styles for rendering the Tile control.

2)  Create an HTML page and add the scripts and css references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Typescript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>
<body>
    <!--Add Tile here-->
</body>
</html>

{% endhighlight %}

3)	Add the below mentioned code with in the <body> tag to render the Tile control with tile text, size and image.

    {% highlight html %}

        <div class="e-tile-column">
                <div id="tile1"></div> 
        </div>

    {% endhighlight %}

Initialize the Tile in ts file by using the ej.Tile method.

{% highlight ts %}
     
     /// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module TileComponent {
    $(function () {
        var tile1 = new ej.Tile($("#tile1"), {
            tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/map.png',
	     caption:{text:"Maps"}       
       });
   });
}

{% endhighlight %}

Get the following output from the above mentioned code

![](Getting-Started_images/Getting-Started_img1.png)

You can easily design a home page using tile control for easy navigation. Therefore, you require many different sizes of tiles aligned in a grid-like manner. The tiles will be aligned automatically to define the necessary tile elements inside the wrapper element, that contains a column class. You can define all columns elements under the wrapper element with the tile group class to make ‘n’ number of tiles as a grouped tile. Add the below mentioned code to the corresponding view page.

{% highlight html %}
    
    <div id="scrollTarget">
        <div class="e-tile-group">
            <div class="e-tile-column">
                <div id="tile1"></div>
                <div class="e-tile-small-col-2">
                    <div id="tile2"></div>
                    <div id="tile3"></div>
                    <div id="tile4"></div>
                    <div id="tile5"></div>
                </div>
                <div id="tile6"></div>
                <div id="tile7"></div>
                <div id="tile8"></div>
            </div>
            <div class="e-tile-column">
                <div id="tile9"></div>
                <div id="tile10"></div>
                <div id="tile11"></div>
                <div id="tile12"></div>
                <div id="tile13"></div>
            </div>
        </div>
    </div>      
 
{% endhighlight %}

{% highlight ts %}
     
 /// <reference path="../tsfiles/jquery.d.ts" />
 /// <reference path="../tsfiles/ej.web.all.d.ts" />\

module TileComponent {
    $(function () {
        var tile1 = new ej.Tile($("#tile1"), {
            imagePosition:"fill",
			caption:{text:"People"},
			tileSize:"medium",
            imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/people_1.png',
        });
		var tile2 = new ej.Tile($("#tile2"), {
            imagePosition:"center",		
			tileSize:"small",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/alerts.png',		 
	
        });
		var tile3 = new ej.Tile($("#tile3"), {
            imagePosition:"center",		 
			tileSize:"small",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/bing.png',		 
        });
		var tile4 = new ej.Tile($("#tile4"), {
            tileSize:"small",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/camera.png',		 
        });
		var tile5 = new ej.Tile($("#tile5"), {
            imagePosition:"center",		 
			tileSize:"small",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/messages.png',		 
        });
		var tile6 = new ej.Tile($("#tile6"), {
            imagePosition:"center",		 
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/games.png',	
			caption:{text:"Play"}
        });
		var tile7 = new ej.Tile($("#tile7"), {	 
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/map.png',
			caption:{text:"Maps"}
        });
		var tile8 = new ej.Tile($("#tile8"), {
            imagePosition:"fill",		 
			tileSize:"wide",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/sports.png',
			caption:{text:"Sports"}
        });
		var tile9 = new ej.Tile($("#tile9"), {
            imagePosition:"fill",
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/people_2.png',
			caption:{text:"People"}
        });
		var tile10 = new ej.Tile($("#tile10"), {
            imagePosition:"center",
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/pictures.png',
			caption:{text:"Photo"}
        });
		var tile11 = new ej.Tile($("#tile11"), {
            imagePosition:"center",
			tileSize:"wide",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/weather.png',
			caption:{text:"Weather"}
        });
		var tile12 = new ej.Tile($("#tile12"), {
            imagePosition:"center",
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/music.png',
			caption:{text:"Music"}
        });
		var tile13 = new ej.Tile($("#tile13"), {
            imagePosition:"center",
			tileSize:"medium",
            imageUrl:'http://js.syncfusion.com/ug/web/content/tile/favs.png',
			caption:{text:"Favorites"}
        });
    });
}

{% endhighlight %}

Run the above code to get the following output.

![](Getting-Started_images/Getting-Started_img2.png)


N> You can find the Tile control properties from the [API reference](https://help.syncfusion.com/api/js/ejtile).
