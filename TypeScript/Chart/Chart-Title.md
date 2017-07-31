---
layout: post
title: Chart Title
description: How to customize the chart title.
platform: typescript
control: Chart
documentation: ug
---

# Chart Title & Subtitle

## Title

By using the title option, you can add the [`text`](../api/ejchart.html#members:title-text) as well as customize its [`border`](../api/ejchart.html#members:title-border),  [`background`](../api/ejchart.html#members:title-background) color and [`font`](../api/ejchart.html#members:title-font).

{% highlight javascript %}
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ChartComponent {
    $(function () {
        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
             // ... 
             title: { 
                  //Adding text to chart title
                 text: 'Efficiency of oil-fired power production ', 
                  //Change the title text background color
                 background : "lightblue",
                  //Customizing Chart title border
                border: { 
                           color: "blue",
                           width: 2,
                           opacity: 0.5 ,
                           cornerRadius : 4
                         },
 
                  //Customizing Chart title font 
                 font:{ 
                         opacity: 1,
                         fontFamily: "Arial",
                         fontStyle: 'italic',
                         fontWeight: 'regular',
                         color: "#E27F2D",
                         size: '23px' 
                     },
               }, 
        // ... 

 });
});
}

{% endhighlight %}

![](Chart-Title_images/Chart-Title_img1.png)

We can trim, wrap and wrapAndTrim to the chart title using textOverflow property. The original text will be displayed as tooltip on mouse hover.


{% highlight javascript %}

     var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
        {
            // ...

            title: {
                text: 'Efficiency of oil-fired power production ',
                 //To enable the title trim, wrap and wrapandtrim
                enableTrim: true,
                 //Setting maximum width to the title
                maximumWidth: 150,
                 //To trim the title
                textOverflow: "trim",
            },

            // ...

        });


{% endhighlight %}

![](Chart-Title_images/Chart-Title_img5.png)


### Title Alignment

You can change the title alignment to *center*, *far* and *near* by using the [`textAlignment`](../api/ejchart.html#members:title-textalignment) property of the chart title. 

{% highlight javascript %}


     var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
           
          //  ...
          
           title: {
                //Change title text alignment
                textAlignment: "near",
                //...
            }          

            //  ...   
      });


{% endhighlight %} 

![](Chart-Title_images/Chart-Title_img2.png)


## Add Subtitle to the chart

By using the subTitle option, you can add the [`subTitle`](../api/ejchart.html#members:title-subtitle) to the chart title and customize its [`border`](../api/ejchart.html#members:title-subtitle-border),  [`background`](../api/ejchart.html#members:title-subtitle-background) color and [`font`](../api/ejchart.html#members:title-subtitle-font). 

{% highlight javascript %}

 var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
               
              // ... 
            title: {
                  // ... 
                 subTitle: { 
                           //Add subtitle to chart title 
                            text: "( in a week )", 
                          //Change the title text background color
                            background : "lightblue",
                          //Customizing Chart subtitle border
                            border: { 
                                      color: "blue",
                                      width: 2,
                                      opacity: 0.2 ,
                                      cornerRadius : 4
                           },

                           //Customizing Chart subtitle font 
                              font:{ 
                                     opacity: 1, 
                                     fontFamily: "Arial", 
                                     fontStyle: 'italic',
                                     fontWeight: 'regular', 
                                     color: "#E27F2D", 
                                     size: '12px' 
                                }, 
                              } 
                           } 
                  // ...
 });

{% endhighlight %}

![](Chart-Title_images/Chart-Title_img3.png)

We can trim, wrap and wrapAndTrim to the chart subtitle using textOverflow property. The original text will be displayed as tooltip on mouse hover.

{% highlight javascript %}

        var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
         {
             // ...

             title: {

                 // ...
                 subTitle:{
                     text: '( in a week )', 
                     //To enable the sub-title trim, wrap and wrap and trim
                     enableTrim: true,
                     //Setting maximum width to the sub-title
                     maximumWidth: 50,
                     //To trim the sub-title
                     textOverflow: "wrap",
                 },
             },

             // ...

         });


{% endhighlight %}

![](Chart-Title_images/Chart-Title_img6.png)

### Subtitle Alignment

You can change the subtitle alignment to *center*, *far* and *near* by using the [`textAlignment`](../api/ejchart.html#members:title-subtitle-textalignment) property of the subTitle.

{% highlight javascript %}


     var chartsample = new ej.datavisualization.Chart($("#chartcontainer"), {
    
        //  ...  
        title: {                
             // ...
             subTitle:{
                 //Change subtitle to text aligment
                 textAlignment: "center",		
                 // ...
               }
         }
            
            //  ...   
      });


{% endhighlight %}

![](Chart-Title_images/Chart-Title_img4.png)

