---
layout: post
title: Miscellaneous
description: miscellaneous
platform: Typescript
control: Menu
documentation: ug
---

# Miscellaneous

##Height

Specifies the height of the root menu. You can customize the height of the **Menu** control by using height property. 

You can specify the height of the **Menu** control in the script as follows.


{% highlight javascript %}


/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />


module MenuComponent {
    $(function () {
        var sample = new ej.Menu($("#menu"),{
            height: 50
        });
    });
}

{% endhighlight %}

##Width

Specifies the width of the main menu. You can customize the width of the **Menu** control by using width property.

You can specify the width of the **Menu** control in the script as follows.

{% highlight javascript %}


    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 700
        });
    });


{% endhighlight %}

##Open on click

Specifies the sub menu items to be show or open only on click. It accepts the Boolean value. Its default value is false. If we set “**openOnClick**” property to true then the submenu items will open only on click. By default the submenu will open when we hover on menu items.

Add the following **&lt;script&gt;** in the above code sample. 



{% highlight javascript %}



    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 612,
            openOnClick: true
        });
    });



{% endhighlight %}



Output screenshot for the above code example is as follows.

![](Miscellaneous_images/Miscellaneous_img1.png)


##Animation

**AnimationType** is used to enable or disable the Animation when hover or click on menu items. Its value type is string. It accepts two values such as “none” and “default”. Support to disable the **AnimationType** when hover or click on menu items is none. Support to enable the Animation Type when hover or click on menu items is default. 

Add the following **&lt;script&gt;** in the above sample code. 



{% highlight javascript %}


    $(function () {
        var sample = new ej.Menu($("#menu"),{
            width: 612,
            animationType: ej.AnimationType.Default
        });
    });



{% endhighlight %}


Output screenshot for the above code sample is as follows.

![](Miscellaneous_images/Miscellaneous_img2.png)


##Title text

Specifies the title to the responsive menu. You can provide title to the **Menu** control by using **titleText** property. 

You can specify the title of the **Menu** control in the script as follows.



{% highlight javascript %}


    $(function () {
        var sample = new ej.Menu($("#menu"),{
            titleText: "Title of the Menu"
        });
    });



{% endhighlight %}



The following screenshot displays the output of the above code.

![](Miscellaneous_images/Miscellaneous_img3.png)


##Show root level arrows

Specifies the main menu item arrows to display only when it contains child menu items. You can use “**showRootLevelArrows**” property to display the arrows of main menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

Add the following **&lt;script&gt;** in the above code sample.



{% highlight javascript %}

  $(function () {
        var sample = new ej.Menu($("#menu"),{
                width: 500,
                showRootLevelArrows: false
            });
        });



{% endhighlight %}



The following screenshot displays the output of the above code.

![](Miscellaneous_images/Miscellaneous_img4.png)


##Show sub level arrows

Specifies the sub menu items arrows to display only when it contains child menu items. You can use “**showSubLevelArrows**” property to show the arrows of sub menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

Add the following **&lt;script&gt;** in the sample code.



{% highlight javascript %}


    $(function () {
        var sample = new ej.Menu($("#menu"),{
                width: 500,
                showSubLevelArrows: false
            });
        });



{% endhighlight %}



The following screenshot displays the output of the above code.

![](Miscellaneous_images/Miscellaneous_img5.png)


