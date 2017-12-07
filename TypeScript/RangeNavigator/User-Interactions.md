---
layout: post
title: UserInteraction
description: How to enable and cutomize the scrollbar, selection and highlighting in Essential typescript RangeNavigator.
platform: typescript
control: RangeNavigator
documentation: ug
---

# User Interactions

## Highlight

EjRangeNavigator provides highlighting supports to the intervals on mouse hover. To enable the highlighting option, set the `enable` property to true in the `highlightSettings` of `navigatorStyleSettings`.

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

 $(function () {

    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), { 
     
         //...   
         navigatorStyleSettings:{
                //...        
              highlightSettings:{
                   // enable the highlight settings
                   enable: true                                
              }    
              //...
          }
          // ...             
     });

 });
}

{% endhighlight %}


![](User-Interactions_images/User-Interactions_img1.png) 


[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/highlight) here to view the highlight and selections online demo sample.

### Customize the highlight style

To customize the highlighted intervals, use color, border and opacity options in the `highlightSettings`.

{% highlight javascript %}

    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), { 
     
         //...   
         navigatorStyleSettings:{
                //...        
                highlightSettings:{
                    // enable the highlight settings
                    enable: true,         
                    // customizing style
                    color: '#006fa0',       
                    border:{
                        color: 'red' , width: 2
                      }        
              }
              //...
         }
         // ...             
     });


{% endhighlight %}

![](User-Interactions_images/User-Interactions_img2.png)


## Selection

EjRangeNavigator provides selection supports to the intervals by, clicking and dragging the highlighted intervals. To enable the selection option, set the `enable` property to true in the `selectionSettings`.

{% highlight javascript %}

    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
     
         //...   
         navigatorStyleSettings:{
                //...        
              selectionSettings:{
                   // enable the selection settings
                   enable: true                                
              }    
              //...
          }
          // ...             
     });

{% endhighlight %}


![](User-Interactions_images/User-Interactions_img3.png) 


[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/highlight) here to view the highlight and selections online demo sample.

### Customize the selection style

To customize the selected intervals, use color, border and opacity options in the selectionSettings.

{% highlight javascript %}

   var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), { 
     
         //...   
         navigatorStyleSettings:{
                //...        
                selectionSettings: {
                    // enable the selection settings
                    enable: true,         
                    // customizing style
                    color: '#27e8e5',       
                    border:{
                         color: 'red' , width: 2
                       }
                  //...
              }
         // ...             
     });


{% endhighlight %}

![](User-Interactions_images/User-Interactions_img4.png)


## Scrollbar

* To render the Scrollbar in RangeNavigator, you need to enable `enableScrollbar` option.
 
* `scrollRangeSettings` of  range navigator `start` and `end` value is used to set the minimum and maximum datasource value to be added in the range navigator.
 
* Based on the scrollRangeSettings *start, end* value and dataSource *start, end* value scrollbar will be adjust.

* When you change the scrollbar position, `scrollEnd` event returns the current position of start and end range value.

{% highlight javascript %}

    var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
          
         //...
         //Enable scrollbar option in the range navigator
          enableScrollbar: true,
         //Maximum data to be displayed in the range navigator control
         scrollRangeSettings: {
               start: new Date(2010, 0, 1),
               end: new Date(2011, 10, 31)
           },
           
         //Subscribe the event on scrollbar position changed           
         scrollEnd: "onScrollbarChange"
         
         //...
     });

      function onScrollbarChange(sender) {
            var start  = sender.data.newRange.start;
            var end  = sender.data.newRange.end;
      }

{% endhighlight %}

![](User-Interactions_images/User-Interactions_img5.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/scrollbar) here to view scrollbar online demo sample.