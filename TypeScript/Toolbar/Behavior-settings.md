---
layout: post
title: Behavior-settings
description: behavior settings
platform: TypeScript
control: Toolbar
documentation: ug
---

# Behavior settings

The following are some miscellaneous properties that enables you to change the behavior of **Toolbar** control.

## Enabling Toolbar

The **Toolbar** property **enabled** is used to enable or disable the **Toolbar**. Set the value to this property as **Boolean** type.

{% highlight html %}

<div class="cols-sample-area">
   <div id="toolbar">
      <ul>
         <li id="Left" title="Left">
            <div class="ToolbarItems LeftAlign_tool"></div>
         </li>
         <li id="Center" title="Center">
            <div class="ToolbarItems CenterAlign_tool"></div>
         </li>
         <li id="Right" title="Right">
            <div class="ToolbarItems RightAlign_tool"></div>
         </li>
         <li id="Justify" title="Justify">
            <div class="ToolbarItems Justify_tool"></div>
         </li>
      </ul>
      <ul>
         <li id="Bold" title="Bold">
            <div class="ToolbarItems Bold_tool"></div>
         </li>
         <li id="Italic" title="Italic">
            <div class="ToolbarItems Italic_tool"></div>
         </li>
         <li id="StrikeThrough" title="Strike Through">
            <div class="ToolbarItems StrikeThrough_tool"></div>
         </li>
         <li id="UndeLine" title="UnderLine">
            <div class="ToolbarItems Underline_tool"></div>
         </li>
      </ul>
   </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        // declaration
        var sample = new ej.Toolbar($("#toolbar"),{
            enabled: true
         });
    });

{% endhighlight %}

{% highlight css %}

<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}

## Hiding Toolbar 

The **Toolbar** property **hide** is used to show or hide the **Toolbar**. Set the value to this property as **Boolean** type.


{% highlight javascript %}

    $(function () {
        // declaration
       var sample = new ej.Toolbar($("#toolbar"),{
            hide: true
         });
    });

{% endhighlight %}