---
layout: post
title: Getting Started RadioButton | Typescript | Syncfusion
description: Getting Started
platform: TypeScript
control: RadioButton
documentation: ug
---

# Getting Started

This section discloses the details on how to render and configure a **RadioButton component** in a TypeScript application.

## Create your first Radio Button	

* Create a TypeScript application and refer the dependent modules, script and CSS with the help of given [Getting started documentation](https://help.syncfusion.com/js/typescript).

* In the index.HTML file, add the below input element for rendering RadioButton component,

{% highlight html %}

    <div>
        <br />
        Category
        <br />
        <br />
        <table>
            <tr>
                <td>
                    <input type="radio" id="Radio1" />
                    <label for="Radio1">Fresher</label>
                </td>
                <td colspan="2">
                    <input type="radio" id="Radio2" />
                    <label for="Radio2">Experienced</label>
                </td>
            </tr>
        </table>
        <br />
        <br />
        Experienced
        <br />
        <br />
        <table>
            <tr>
                <td>
                    <input type="radio" id="Radio3" />
                    <label for="Radio3">1+ years</label>
                </td>
                <td colspan="2">
                    <input type="radio" id="Radio4" />
                    <label for="Radio4">2.5+years</label>
                </td>
                <td colspan="2">
                    <input type="radio" id="Radio5" />
                    <label for="Radio5">5+years</label>
                </td>
            </tr>
        </table>
    </div>      

{% endhighlight %} 

* Create app.ts file and use the below content

{% highlight JS %}

    /// <reference path="tsfiles/jquery.d.ts" />
    /// <reference path="tsfiles/ej.web.all.d.ts" />

    module AppComponent { 
        $(function () {
            new ej.RadioButton($("#Radio1"),{value:"Fresher", name:"Category", size:"small" });
            new ej.RadioButton($("#Radio2"),{value:"Experienced", name:"Category", size: "small", checked:true });
            new ej.RadioButton($("#Radio3"),{value:"1+ years", name:"Experienced", size:"medium", checked: true });
            new ej.RadioButton($("#Radio4"),{value:"2.5+ years", name:"Experienced",size:"medium" });
            new ej.RadioButton($("#Radio5"), {value:"5+ years", name:"Experienced", size:"medium"}); 
        });
    }     

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

    tsc

{% endhighlight %} 

Now build your application, so that the app.ts file will compiled and automtically generated the app.js file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file by compiling build the aplication.

Execution of above code will render the following output.

![](Getting-Started_images/radiobutton.png) 