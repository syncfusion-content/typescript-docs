---
layout: post
title: Selection
description: selection
platform: typescript
control: ListBox
documentation: ug
---

# Selection

The ListBox widget allows you to highlight the selected item. It allows multiple selection also. 


## Selection on initialize

By default, the ListBox widget allows single item selection. We can select specific item during initialization of the ListBox widget using the “selectedIndex” API. 

{% tabs %}
{% highlight html %}

<div>
        <ul id="listbox">
            <li>Audi A4</li>
            <li>Audi A5</li>
            <li>Audi A6</li>
            <li>Audi A7</li>
            <li>Audi A8</li>
            <li>BMW 501</li>
            <li>BMW 502</li>
            <li>BMW 503</li>
            <li>Batch</li>
            <li>BMW 507</li>
            <li>BMW 3200</li>
            <li>Cut</li>
        </ul>
    </div>

{% endhighlight %}

{% highlight javascript %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />\

module ListBoxComponent {
    $(function () {

           var listboxInstance = new ej.ListBox($("#listbox"), {
                
                    selectedIndex: 2
                });
        });

}

{% endhighlight %}
{% endtabs %}

![](Selection_images\Selection_img1.png)

## Multiple selection

Multiple selection can be enabled using “allowMultiSelection” property. You can select multiple list items using <kbd>“Ctrl”</kbd> and <kbd>“Shift”</kbd> keys.

{% seealso %} [Keyboard Interaction](https://help.syncfusion.com/js/listbox/keyboard-interaction). {% endseealso %}

{% highlight javascript %}


             $(function () {

            var listboxInstance = new ej.ListBox($("#listbox"), {
                
                    allowMultiSelection: true
                });
        });



{% endhighlight %}

![](Selection_images\Selection_img2.png)

## Checkbox

The ListBox widget allows selection through checkbox. It can be enabled using “showCheckbox” API.

The specified items can be checked on initialize through “checkedIndices” property. 

{% seealso %} [checkedIndices](https://help.syncfusion.com/api/js/ejlistbox#members:checkedindices). {% endseealso %}

{% highlight javascript %}


        $(function () {

           var listboxInstance = new ej.ListBox($("#listbox"), {
                    showCheckbox: true,
                    checkedIndices: [1, 2]
                });
        });

{% endhighlight %}



![](Selection_images\Selection_img3.png)
