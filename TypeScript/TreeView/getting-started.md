---
layout: post
title: getting-started
description: getting started
platform: js
control: TreeView
documentation: ug
---

# Getting Started



Using the following steps, you can create a **TypeScript** TreeView component.

## Creating an TreeView in TypeScript



You can create a **TypeScript** application with the help of the given [TypeScript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

Within an index.html file and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<title>TypeScript Application</title>
<link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
<script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>

</head>
<body>
<!--Add TreeView sample  here-->
</body>
</html>


{% endhighlight %}



Execute the below steps to render the TreeView control in TypeScript.

{% highlight html %}

  <div style="width: 250px; max-width:100%">
        <ul id="treeView">
            <li class="expanded">
                Artwork
                <ul>
                    <li>
                        Abstract
                        <ul>
                            <li>2 Acrylic Mediums</li>
                            <li>Creative Acrylic</li>
                            <li>Modern Painting</li>
                            <li>Canvas Art</li>
                            <li>Black white</li>
                        </ul>
                    </li>
                    <li>
                        Children
                        <ul>
                            <li>Preschool Crafts</li>
                            <li>School-age Crafts</li>
                            <li>Fabulous Toddler</li>
                        </ul>
                    </li>
                    <li>
                        Comic / Cartoon
                        <ul>
                            <li>Batman</li>
                            <li>Adventures of Superman</li>
                            <li>Super boy</li>
                        </ul>
                    </li>
                </ul>
            </li>
            <li class="expanded">
                Books
                <ul>
                    <li>
                        Comics
                        <ul>
                            <li>The Flash</li>
                            <li>Human Target</li>
                            <li>Birds of Prey</li>
                        </ul>
                    </li>
                    <li>Entertaining</li>
                    <li>Design</li>
                </ul>
            </li>
            <li>
                Music
                <ul>
                    <li>
                        Classical
                        <ul>
                            <li>Medieval</li>
                            <li>Orchestral</li>
                        </ul>
                    </li>
                    <li>Mass</li>
                    <li>Folk</li>
                </ul>
            </li>
        </ul>
    </div>
<script src="app.js"></script>

{% endhighlight %}



* Create app.ts file and use the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {
        });
    });
}

{% endhighlight %}



* Now build your application, so that the **app.ts** file will compiled and automatically generated the **app.js** file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file by compiling     build the application.



Execution of above code will render the following output.

![](getting-started_images/getting-started_img1.png)


## Drag and Drop

You can drag and drop tree nodes between two TreeView by setting allowDragAndDrop as true along with allowDragAndDropAcrossControl as true.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {
            allowEditing: true,
            allowDragAndDrop: true,
            allowDropChild: true,
            allowDropSibling: true,
        });
    });
}
{% endhighlight %}

## Checkboxes

TreeView consists of in-build checkbox option and it can be displayed to the left of the tree node by setting the showCheckbox property as true. It allows you to select more than one node at a time.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TreeViewComponent {
    $(function () {
        var tree = new ej.TreeView($("#treeView"), {
          showCheckbox : true,
          autoCheckParentNode : true
        });
    });
}

{% endhighlight %}
