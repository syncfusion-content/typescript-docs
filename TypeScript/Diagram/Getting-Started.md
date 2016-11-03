---
title: Getting Started for TypeScript Diagram
description: How to create a Diagram with nodes, connectors.
platform: TypeScript
control: Diagram
documentation: ug
keywords: ejdiagram, js diagram, diagram
---

# Getting started

This section explains briefly about how to create a **Diagram** control in your application with **TypeScript**.

## Adding Script Reference

Create an **HTML** page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
        <link href="http://cdn.syncfusion.com/14.3.0.49/js/web/bootstrap-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
        <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
        <script src="https://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
        <script src="http://js.syncfusion.com/demos/web/scripts/xljsondata.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/14.3.0.49/js/web/ej.web.all.min.js" type="text/javascript"></script>
        <script src="app.js"></script> 
</head>
<body>
</body>
</html>

{% endhighlight %}

In the above code, `ej.web.all.min.js` script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/# "") utility to generate a custom script file with the required widgets for deployment purpose.

## Initialize Diagram

Add a `div` container to render the Diagram.

{% highlight html %}
<!DOCTYPE html>
<html>    
     <body>
        <div id="diagram"></div>
     </body>
</html>

{% endhighlight %}

Initialize the Diagram in ts file by using the `ej.diagram` method. The Diagram is rendered based on default `width` and `height`.

{% highlight html %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />
$(function () {
    var diagram = new ej.datavisualization.Diagram($("#diagram"), {
        width: "1000px",
        height: "600px"        
    });
});

{% endhighlight %}

This creates an empty diagram as shown in image

![](Getting-Started_images/Getting-Started_img1.png)

## Populate Diagram with nodes and connectors

* This section explains how to populate JSON data to the Diagram. 

* The Diagram is rendered based on default `width` and `height`. You can also customize the Diagram dimension by setting the `width` and `height` attribute in `scrollSettings`.

{% highlight html %}
<!DOCTYPE html>
<html>    
     <body>
     <script type="text/javascript" src="diagram/diagram.js">
     </script>
        <div id="diagram"></div>
     </body>
</html>

{% endhighlight %}

{% highlight javascript %}

$(function () {
    var diagram = new ej.datavisualization.Diagram($("#diagram"), {
        width: "1000px",
        height: "600px",
        nodes: [
            createNode({ name: "Start", offsetX: 300, offsetY: 50, width: 140, height: 50, labels: [{ text: "Start" }], type: "flow", shape: "terminator"}),
            createNode({ name: "Init", offsetX: 300, offsetY: 140, width: 140, height: 50, labels: [{ text: "var i = 0;" }], type: "flow", shape: "process" }),
              ],
        connectors: [
            createConnector({ name: "connector1", sourceNode: "Start", targetNode: "Init" }),
          ]
    });
});

function createNode(option: ej.datavisualization.Diagram.Node) {
    return option;
}
function createConnector(option: ej.datavisualization.Diagram.Connector) {
    return option;
}
function createLabel(options : any) {
    return options;
}

{% endhighlight %}

![](Getting-Started_images/Getting-Started_img2.png)