---
layout: post
title: Selection
description: selection
platform: Typescript
control: ListView
documentation: ug
---

# Selection

**MultiSelection**

**ListView** has a checklist feature that is used to select multiple list items at the same time in the **ListView**. For this, set **data-ej-enableCheckMark** attribute to **“True”**.

Refer the following code examples.



{% highlight html %}


    <div id="defaultlistview">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}
/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />
module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#defaultlistview"), {
                enableCheckMark: true, 
                width: 400
             });
        });
}

{% endhighlight %}



Run the codes to get the following output

![](Selection_images/Selection_img1.png) 

**PreventSelection**

When selecting a specific list item, it is highlighted with an active color. **data-ej-preventSelection** attribute is used to prevent this behavior by setting it to **“True”**. 

N> When the click or select action is completed, the highlight is undone automatically even when the  attribute is set to “False”.

Refer the following code examples.



{% highlight html %}


    <div id="defaultlistview">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#defaultlistview"), {
                 preventSelection: true, 
                 width: 400
             });
        });
}
{% endhighlight %}



**PersistSelection**

**data-ej-persistSelection** attribute is used to highlight the selected item in the **ListView** control even after touch end happens. By default, the active state is removed once the touch end happens.

Refer the following code examples.



{% highlight html %}


    <div id="defaultlistview">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}
    
    $(function () {
        var sample = new ej.ListView($("#defaultlistview"), {
                 persistSelection: true, 
                 width: 400 
            });
        });

{% endhighlight %}



Run the codes to get the following output

![](Selection_images/Selection_img2.png) 

