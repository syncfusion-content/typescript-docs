---
layout: post
title: Localization of Essential TypeScript Chart
description: Learn how to localize chart based on a specific culture.
platform: typescript
control: Chart
documentation: ug
---

# Localization

EjChart supports localization for its axis labels and tooltip. To render the chart with specific culture you have to refer the corresponding **globalize** culture script and need to specify the culture name in [`locale`](../api/ejchart#members:locale) property of chart.   

{% highlight html %}


<head> 
<!--Refer french globalize culture script-->
<script src="../scripts/cultures/globalize.culture.fr-FR.min.js"></script>
</head>

<body>
    <div id="chartcontainer"></div>
   
<script>
    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
                  //  ...
                  //Render chart in french locale
                  locale: 'fr-FR',
      });
  </script>

</body>


{% endhighlight %}

![](Localization_images/Localization_img1.png)




