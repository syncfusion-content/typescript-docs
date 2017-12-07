---
layout: post
title: Appearance-And-Styling
description: Appearance And Styling
platform: typescript
control: RangeNavigator
documentation: ug
---

### Appearance and Styling

**RangeNavigator** is enriched with lots of customization options for labels, gridlines and slider to develop high quality graphic rich control.

#### Customize labels

The labels are found along the range, displaying the value of the data it correspond, both on (higher level label) and below (lower level label) the **RangeNavigator**. **RangeNavigator** labels are further customized using "**font**" property in label Settings. 

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts"></reference>
/// <reference path="../tsfiles/ej.web.all.d.ts"></reference>

module RangeComponent {

       $(function () {

        var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
        // ...             
        labelSettings: {
            // customizing higher level labels.
            higherLevel: {
                style: {
                    font: {
                        color: '#ff0000',
                        style: 'Normal',
                        size: '12px',
                        opacity: 1,
                        weight: 'regular'
                    },
        
                },
            },
            // customizing lower level labels.
            lowerLevel: {
                style: {
                    font: {
                        color: '#ff0000',
                        style: 'Normal',
                        size: '12px',
                        opacity: 1,
                        weight: 'regular'
                    },
                },
            }
        },
        // ...             
        
        });
        });
 }

{% endhighlight %}

![](Appearance-And-Styling_images/Appearance-And-Styling_img1.png) 


##### Label Placement

Labels in **RangeNavigator** are placed inside or outside of the control. You can customize both the higher and lower level labels using **labelPlacement** property in label setting of **RangeNavigator**. By default **labelPlacement** is "outside" for the both higher and lower level labels.

The following screen shot illustrates both the lower and higher level labels that are placed outside the control with **labelPlacement** specified as outside.

{% highlight javascript %}

       var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
        // ...             
        labelSettings: {
            higherLevel: {
                labelPlacement: "inside",
            },
            lowerLevel: {
                labelPlacement: "inside"
            }
        },
        // ...             
        
        });
        });

{% endhighlight %}


The following screenshot illustrates a **RangeNavigator** with labels inside the control after specifying the **labelPlacement** as inside.



![](Appearance-And-Styling_images/Appearance-And-Styling_img2.png) 

#### Customize RangeNavigator

RangeNavigator is customized using **navigatorStyleSettings** properties. You can customize the selected and unselected region color using **selectedRegionColor**, **unselectedRegionColor** in **navigatorStyleSettings** and the thumb of the slider using **thumbColor, thumbRadius** and **thumbStroke** in **navigatorStyleSettings.  majorGridLineStyle** and **minorGridLineStyle**  are used to customize the grid line color and visibility.

{% highlight javascript %}

       var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
        // ...    
        //  To customize the navigator element     
        navigatorStyleSettings: {
        
            unselectedRegionColor: "white",
            selectedRegionColor: "#5EABDE",
            thumbColor: "white",
            thumbRadius: 10,
            thumbStroke: "#303030",
            background: "transparent",
            border: {
                color: "black",
                width: 3
            },
            majorGridLineStyle: {
                color: "transparent"
            },
            minorGridLineStyle: {
                color: "transparent"
            }
        },
        //  To customize the labels
        labelSettings: {
        
            higherLevel: {
                style: {
                    font: {
                        color: 'black',
                        size: '13px',
                        opacity: 1
                    },
                    horizontalAlignment: "left"
                },
                intervalType: 'years',
                labelPlacement: "inside"
            },
            lowerLevel: {
                style: {
                    font: {
                        color: 'black',
                        size: '12px',
                        opacity: 1
                    },
                    horizontalAlignment: "center"
                },
                intervalType: 'quarters',
                labelPlacement: "inside"
            }
        },
        
        // ...             
        
        });
        });


{% endhighlight %}



![](Appearance-And-Styling_images/Appearance-And-Styling_img3.png) 

#### Themes

**RangeNavigator** theme is a set of pre-defined options that are applied to the control before each **RangeNavigator** is instantiated. Following predefined themes are available in JavaScript **RangeNavigator**.

1. flat light
2. flat dark
3. gradient light 
4. gradient dark 
5. azure                      
6. azure dark               
7. lime 
8. lime dark
9. saffron
10. saffron dark
11. gradient azure
12. gradient azure dark
13. gradient lime
14. gradient lime dark
15. gradient saffron
16. gradient saffron dark

{% highlight javascript %}


              var sample = new ej.datavisualization.RangeNavigator($("#RangeNavigator"), {
                   // ...              
                      theme: 'saffron',
                   // ...             
               });


{% endhighlight %}



![](Appearance-And-Styling_images/Appearance-And-Styling_img4.png) 
