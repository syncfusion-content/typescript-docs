---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: TypeScript
control: DateTimePicker
documentation: ug 
---

# Appearance and Styling

## Theme

**DateTimePicker** control support rich appearance. This control consist of six flat themes and six gradient themes. To use these twelve themes, refer the themes files in HTML file. 

You need two style sheets to apply styles to **DateTimePicker** control; one **ej.widgets.core.min.css** and one **ej.theme.min.css**. If you use **ej.widgets.all.min.css** then you don’t need to use **ej.widgets.core.min.css** and **ej.theme.min.css** because **ej.widgets.all.min.css** is a combination of these two.

The core style sheet applies styles related to positioning and size, but are not related to the color scheme and always require the control to look correct and function properly. The theme styles sheet applies theme-specific styles like colors and backgrounds.

The following list is of the twelve themes supported by **DateTimePicker**:

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark


Add the following code in your **HTML** page.



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
   <head>
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
   </head>
   <body>
      <div class="control">
         <input type="text" id="dateTime" />
      </div>
      <script>
      /// <reference path="tsfiles/jquery.d.ts" />
      /// <reference path="tsfiles/ej.web.all.d.ts" />

module DateTimePickerComponent {
         $(function () {
             // declaration
              var datetimeSample = new ej.DateTimePicker($("#datetimepick"), {
                 width: '200px'
             });
         });
}
      </script>
   </body>
</html>

{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

![](Appearance-and-Styling_images/Appearance-and-Styling_img1.png)

## CSS Class

**DateTimePicker** control also allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds. To apply custom themes you have a property called **cssClass**. **cssClass** property sets the root class for **DateTimePicker** theme.

Using this **cssClass** you can override the existing styles under the theme style sheet. The theme style sheet applies theme-specific styles like colors and backgrounds. In the following example, the value of **cssClass** property is set as “**Purple-dark**”. **Purple-dark** is added as root class to **DateTimePicker** control at the runtime. From this root class you can customize the **DateTimePicker** control theme.

Add the following code in your **HTML** page to render the DateTimePicker.

{% highlight html %}
   
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
   <head>
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
   </head>
   <body>
      <div class="control">
         <input type="text" id="dateTime" />
      </div>
      <script>
         $(function () {
             // Add the code in your script section to render the DateTimePicker with cssClass property
              var datetimeSample = new ej.DateTimePicker($("#datetimepick"), {
                 width: 200,
                 cssClass: "Purple-dark"
             });
         });
      </script>
   </body>
</html>

{% endhighlight %}



In the following style sheet the exiting theme style sheet file has been over-ridden using root class “**Purple-dark**”. 

Add the following code in your style section.

{% highlight css %}

<style>
   .Purple-dark .e-week-header {
         color: #EBADD6;
   }
   .Purple-dark .e-text {
         color: black;
   }
   .Purple-dark .e-state-default {
         color: pink;
   }
   .Purple-dark .e-active {
         background-color: #FF1975;
   }
   .Purple-dark .e-state-default:hover {
         color: #EBADD6;
   }
   .Purple-dark .e-dt-button {
         color: black;
         background-color: #E085C2;
   }
   .Purple-dark .e-header {
         background-color: #E085C2;
         color: black;
   }
   .Purple-dark .e-timecontainer .e-header {
         background-color: #E085C2;
         color: black;
   }
   .Purple-dark .e-datepicker table td:hover,
   .Purple-dark .e-datepicker td.e-state-hover,
   .Purple-dark .e-datepicker .current-month.e-state-default.e-special-day:hover {
         background-color: #FF1975;
   }
   .Purple-dark .e-timewidget .e-select:hover,
   .Purple-dark .e-time-popup.e-popup .e-hover {
         background: #FF1975;
         color: white;
   }
   .Purple-dark .e-datetime-wrap:hover {
         background: #FF1975;
   }
</style>

{% endhighlight %}



![](Appearance-and-Styling_images/Appearance-and-Styling_img2.png)

