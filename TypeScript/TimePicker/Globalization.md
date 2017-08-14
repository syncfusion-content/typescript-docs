---
layout: post
title: Localization
description: localization
platform: TypeScript
control: TimePicker
documentation: ug
---

# Globalization

**TimePicker** supports globalization with different culture.

## Enabling Globalization Support

The following steps explains you on how to enable **Globalization** support for **TimePicker**.

In an **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.   


{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}


{% highlight html %}

<html>
<head>
    <!--You can enable localization property using the following code example.-->
    <title>Essential Studio for JavaScript : Timepicker </title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="https://cdn.syncfusion.com/js/assets/i18n/ej.culture.zh-CN.min.js"></script>
</head>
<body>
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <div class="control">
                        <input type="text" id="time" accesskey="j"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <script type="text/javascript">
    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
        $(function () {
             var timeSample = new ej.TimePicker($("#timepick"), {
                locale: "zh-CN"
            });
        });
}
    </script>
</body>
</html>

{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects. jQuery.globalize has been removed from version 13.4.0.53 onwards. For version lower than 13.4.0.53, refer jQuery.globalize.min.js along with ej.web.all.min.js to support globalization.

Execute the above code to render the following output.

![](Globalization_images/Globalization_img1.png) 

