---
layout: post
title: Exporting
description: exporting
platform: typescript
control: Circular Gauge
documentation: ug
---

# Exporting

**Circular Gauge** has an exporting feature that converts **Gauge** control into image format and then export in client side. The method API `exportImage` is used to export the **Circular Gauge**. It has two arguments such as **file name** and **file format** to specify the file name and file formats. For exporting refer the following code example.

{% highlight html %}

<input type="submit" value="Export Image" id="buttonExportImage">
    <div id=" circularGauge "></div>
    <div id="txtFileName">FileName </div>
    <div id="ddFileType">FileFormat </div>
</input>
<select id="Select1">
    <option value="JPEG">JPEG</option>
    <option value="PNG">PNG</option>
</select>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        var circularGaugeSample = new ej.datavisualization.CircularGauge($("#circularGauge"));
        var basicButton = new ej.Button($("#buttonExportImage"), {
            width: "100px", click: "buttonClickEvent", 
            });
    });
    function buttonClickEvent() {
        var FileName = $("#txtFileName").val();
        var FileFormat = $("#ddFileType").val();
         var circularGaugeSample = new ej.datavisualization.CircularGauge($("#circularGauge"));
         circularGaugeSample.exportImage(FileName,FileFormat);
        
    }

{% endhighlight %}


Execute the above code to render the following output.

![](Exporting_images/Exporting_img1.png)

