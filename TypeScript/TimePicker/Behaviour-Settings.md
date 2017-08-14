---
layout: post
title: Behaviour-Settings
description: behaviour settings
platform: TypeScript
control: TimePicker
documentation: ug
---

# Behavior Settings

## Set value of the TimePicker widget

You can use value property to set default time for the **TimePicker**.

The following steps explains you on how to set the default value of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

 <input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TimePickerComponent {
    // Set default value of the TimePicker as follows.
    $(function () {
         var timeSample = new ej.TimePicker($("#timepick"), {
            value: "10:10 AM"
        });
    });
});
}

{% endhighlight %}


![](Behaviour-Settings_images/Behaviour-Settings_img1.png) 

## Enable/Disable TimePicker widget

**TimePicker** widget provides you an option to enable /disable the widget. You can disable the TimePicker by setting the “**enabled**” property value as **false**.

The following steps explain you to enable/disable property in **TimePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}


 <input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // To enable/disable TimePicker controls use the following code example.
    //Enable Timepicker:
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
        });
        timeSample.enable();
    });
    //Disable Timepicker:
    $(function () {
         var timeSample = new ej.TimePicker($("#timepick"), {
        });
        timeSample.disable();
    });

{% endhighlight %}


Execute the above code to render the following output.

![](Behaviour-Settings_images/Behaviour-Settings_img2.png) 

![](Behaviour-Settings_images/Behaviour-Settings_img3.png) 

## Restrict editing

**TimePicker** widget provides **readOnly** property to disable editing in the control. Therefore you can only read the value set to **TimePicker** and cannot modify it. The **value** property allows you to set the default value for **TimePicker** widget when it is created.

### Configure TimePicker textbox to restrict editing

The following steps allows you to disable editing value in **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Configure TimePicker textbox to restrict editing as follows,
   var timeSample = new ej.TimePicker($("#timepick"), {
        readOnly: true
    });
    
{% endhighlight %}


The following screenshot illustrates a **TimePicker** textbox configured to restrict editing.

![](Behaviour-Settings_images/Behaviour-Settings_img4.png) 

## Rounded Corner

You can customize the shape of the **TimePicker** widget from regular rectangular shape to rounded rectangle shape using **showRoundedCorner** property that is set to **false** by default.

### Configure Rounded corner to TimePicker Text box

The following steps explain you to change the edges of the textbox to rounded corner.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // You can configure Rounded Corner  in TimePicker control as follows,
   var timeSample = new ej.TimePicker($("#timepick"), {
        showRoundedCorner: true,
    });

{% endhighlight %}


The following screenshot illustrates a **TimePicker** when **showRoundedCorner** is set to “**true**”.

![](Behaviour-Settings_images/Behaviour-Settings_img5.png) 

## Scaling

**TimePicker** widget provides you options to change its height, width and also to change popup height and width.

### Change TimePicker widget Height and width

You can use **height** and **width** property to customize **TimePicker** width and height.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // You can customize the width and height of the TimePicker as follows.
    $(function () {
       var timeSample = new ej.TimePicker($("#timepick"), {
            width: 150,
            height: 50
        });
    });
    
{% endhighlight %}


Execute the above code to render the following output.

![](Behaviour-Settings_images/Behaviour-Settings_img6.png) 

### Changing TimePicker PopupHeight and PopupWidth

You can use **popupHeight** and **popupWidth** property to customize **TimePicker popup** width and height.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Use popupHeight and popupWidth property for the TimePicker as follows.
    $(function () {
       var timeSample = new ej.TimePicker($("#timepick"), {
            popupHeight: 170,
            popupWidth: 120
        });
    });
    
{% endhighlight %}


Execute the above code to render the following output.

![](Behaviour-Settings_images/Behaviour-Settings_img7.png) 

## State persistence

**TimePicker** widget provide options to maintain the selected value after you refresh the page by using **enablePersistence** property.

### Steps to use State persistence of the TimePicker

The following steps explains you to use **enablePersistence** property.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Use enablePersistence property to maintain selected value as follows.
    $(function () {
       var timeSample = new ej.TimePicker($("#timepick"), {
            value: "10:00 AM",
            enablePersistence: true
        });
    });
    
{% endhighlight %}


## Strict mode of the TimePicker

**TimePicker** widget provides you an option to set default value when there is no default value between minTime and maxTime by using **enableStrictMode** property.  

### Steps to use StrictMode property

The following steps explains you to use strict mode property.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Use enableStrictMode property to set default value as follows.
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
            value: "9:00 AM",
            enableStrictMode: true,
            minTime: "10:00 AM",
            maxTime: "9:00 PM"
        });
    });
    
{% endhighlight %}

Execute the above code to render the following output.


![](Behaviour-Settings_images/Behaviour-Settings_img8.png) 

## Interval

**TimePicker** widget provides you an option to change the interval of the hour, minute and seconds. 

### Steps to change the Time interval of the TimePicker control

The following steps explains you to change the Time Interval of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Change Time Interval using hourInterval, minuteInterval and secondInterval property.
    $(function () {
        var timeSample = new ej.TimePicker($("#timepick"), {
            timeFormat: "h:mm:ss tt",
            hourInterval: 2,
            minutesInterval: 30,
            secondsInterval: 20
        });
    });

![](Behaviour-Settings_images/Behaviour-Settings_img9.png)
    
{% endhighlight %}

