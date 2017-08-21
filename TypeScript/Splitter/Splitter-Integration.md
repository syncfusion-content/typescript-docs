---
layout: post
title: Splitter-Integration
description: splitter integration
platform: Typescript
control: Splitter
documentation: ug
---

# Splitter Integration

The **Splitter** allows you to use other **Essential JavaScript** products inside the pane. The integrated function of those widgets can be used in other panes of the **Splitter**.

## Configuring other widgets in Splitter

The following steps explain the implementation of **Splitter** integration.

In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** with two panes. The first pane has the **TreeView** content and the next one has some content that is related to **TreeView**.

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 20px;">
            <h3> JavaScript </h3>
            <ul id="treeview">
                <li>
                    Tools
                    <ul>
                        <li id="tools" class="_child">Description</li>
                    </ul>
                </li>
                <li>
                    Chart
                    <ul>
                        <li id="chart" class="_child">Description </li>
                    </ul>
                </li>
                <li>
                    Grid
                    <ul>
                        <li id="grid" class="_child">Description</li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
    <div>
        <div style="padding: 20px">
            <div class="_content">
                Select any product from the tree to show the description.
            </div>
            <div class="tools" style="display: none">
                <h3>Tools</h3>
                Essential Tools is an collection of user interface components used to create interactive
                JavaScript applications.
            </div>
            <div class="chart" style="display: none">
                <h3>Chart</h3>
                Essential Chart is a business-oriented charting component.
            </div>
            <div class="grid" style="display: none">
                <h3>Grid</h3>
                Essential JavaScript Grid offers full featured a Grid control with extensive support for
                Grouping and the display of hierarchical data.
            </div>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module SplitterComponent {
    $(function () {
        var treeviewInstance = new ej.Splitter($("#treeview"), {
             nodeSelect: "treeClicked"
              }); /* Render TreeView inside Splitter pane */
        
         var splitter = new ej.Splitter($("#innerSpliter"), {
                height: 280, width: 500,
                properties: [{ paneSize: 200 }]
        });
    });
} 
        function treeClicked(sender, args) { //nodeSelect event handle
            if (sender.currentElement.hasClass('_child')) {
                var content = $('.' + sender.currentElement[0].id).html();
                $('._content').html(content);
            }
        }

{% endhighlight %}

When the node is selected in **TreeView**, the integrated output is displayed in the second pane.

![](Splitter-Integration_images/Splitter-Integration_img1.png) 

![](Splitter-Integration_images/Splitter-Integration_img2.png) 

