---
layout: post
title: Templates
description: templates
platform: typescript
control: ListBox
documentation: ug
---

# Templates

The ListBox widget’s appearance can be customized based on different needs using templates. The desired templates can be defined using the “template” property.

{% highlight html %}
   <ul id="listbox"></ul>
    <script type="text/javascript">
        var data = [{
            text: "Erik Linden",
            imageName: "3",
            designation: "Representative",
            country: "England"
        },
            { text: "John Linden", imageName: "6", designation: "Representative", country: "Norway" },
            { text: "Louis", imageName: "7", designation: "Representative", country: "Australia" },
            { text: "Lawrence", imageName: "8", designation: "Representative", country: "India" }];
        $(function () {
            var listboxInstance = new ej.ListBox($("#listbox"), {
                dataSource: data,
                height: "240",
                width: "350",
                //defining templates
                template: '<div><img class="image" src="images/Employees/${imageName}.png" alt="employee"/>' + '<div class="text"> ${text} </div><div class="desig">${designation}</div><div class="country"> ${country} </div></div>'
            });
        });
    </script>

{% endhighlight %}



N> In the above code snippet, the image path (images/Employees) is given just for demonstration. Hence the images will not be displayed while using the above code.

{% seealso %} [Data Binding](https://help.syncfusion.com/js/listbox/databinding). {% endseealso %}

Define the styles for the template as below.

{% highlight css %}

        .image
        {
            margin:0;
            padding: 3px 10px 3px 3px;
            border:0 none;
            width:60px;
            height:60px;
            float:left;
        }
        .text
        {
             font-weight:bold;
             padding:6px 3px 1px 3px;
        }
        .desig,.country{
            font-size:smaller;
            padding:3px 3px 0px 0px;
        }

{% endhighlight %}

![](Templates_images\Templates_img1.png)

