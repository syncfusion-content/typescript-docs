---
layout: post
title: Behavior-Settings
description: behavior settings
platform: TypeScript
control: GroupButton
documentation: ug
---

# Behavior Settings

GroupButton has some default behavior settings which helps you to perform more operation by Built-in selection.

## Different modes of button

GroupButton provides the different types of modes called check box mode, radio button mode. Setting a **groupButtonMode** property value to checkbox mode, we can perform the multiple actions in a single group. In this case, you can toggle the all the buttons state and perform the actions, since it all will behave as individual button in a group of button. 

Setting a ButtonMode to radio, we can perform the only single action with all related actions in a group of button.

** Checkbox Mode :** Here, multiple button can be selected, please check with the below use case for this mode.

{% highlight html %}


        <div id="groupButton">

            <ul>

                <li>

                    Daily

                </li>

                <li>

                    Weekly

                </li>

                <li>

                    Monthly

                </li>

            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "checkbox",

                width: "215px"

            });
        });
    }    
{% endhighlight %}

![](Behavior-Settings_images/Behavior-Settings_img1.jpeg)


** Radio Button Mode:** Here, single button only can be selected, Please check with the below use case

{% highlight html %}


        <div id="groupButton">

            <ul>

                <li>

                    Credit Card

                </li>

                <li>

                    Debit Card

                </li>

                <li>

                    Net Banking

                </li>

            </ul>

        </div>

{% endhighlight %}

{% highlight js %}


/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "radiobutton",

                width: "215px"

            });
    });
}
{% endhighlight %}

![](Behavior-Settings_images/Behavior-Settings_img2.jpeg)


## SelectedItemIndex

The state of the button can be changed by clicking on the button. Also the selection state of the button can be achieved by using **selectedItemIndex** API which is used to select the button items in GroupButton based on index. 

This property will accept the array values and its value will be differ based on current mode of Button. If the Button mode is “Radio”, then the selected items can have single value within the array, since we can select a single button only in this mode. Whereas for the “checkbox” mode, the selectedItemIndex can have the multiple values within an array, since multiple button can be in active state in this mode.

** Setting a selectedItemIndex for checkbox mode **

{% highlight html %}

        <div id="groupButton">

            <ul>

                <li>

                    Credit Card

                </li>

                <li>

                    Debit Card

                </li>

                <li>

                    Net Banking

                </li>

            </ul>

        </div>

{% endhighlight %}

** Setting a selectedItemIndex for radio button mode**

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "radiobutton",

                width: "215px",

                selectedItemIndex: [1]

            });
    });
}  

{% endhighlight %}

![](Behavior-Settings_images/Behavior-Settings_img3.jpeg)


## Select and deselect the button items using public method 

Button items in GroupButton can be selected or deselected using available public methods “**selectItem**, **deselectItem**”. These two methods will get the index of targeted button as argument. 

** Select the Button Items  **

{% highlight html %}

        <div id="groupButton">

            <ul>

                <li>

                    Credit Card

                </li>

                <li>

                    Debit Card

                </li>

                <li>

                    Net Banking

                </li>

            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "radiobutton",

                width: "300px",

                selectedItemIndex: [1]

            });
      groupButton.selectItem(0);
    });

}
{% endhighlight %}

** Deselect the Button Items **

{% highlight js %}


            groupButton.deselectItem(0);

{% endhighlight %}

**Select or deselect using id attribute ** 

You can select or deselect the button items based on id of the button items also. Please check with the below code example to know about the selection/deselection based on id attribute

{% highlight html %}

        <div id="groupButton">

            <ul>

                <li id="payment_option_1">

                    Credit Card

                </li>

                <li id="payment_option_2">

                    Debit Card

                </li>

                <li id="payment_option_3">

                    Net Banking

                </li>

            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module GroupButtonComponent {
    $(function () {
        var groupButton = new ej.GroupButton($("#groupButton"), {

                groupButtonMode: "checkbox",

                width: "300px",

            });

            groupButton.selectItem("payment_option_2");

    });
} 

{% endhighlight %}

