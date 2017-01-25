---
layout: post
title: Getting Started | CheckBox | TypesScript | Syncfusion
description: Getting Started
platform: TypeScript
control: CheckBox
documentation: ug
---

# Getting Started

This section discloses the details on how to render and configure a CheckBox component in a TypeScript application.

## Create your first CheckBox	

1. Create a TypeScript application and refer the dependent modules, script and CSS with the help of given getting started document.

2. In the index.HTML file, add the input element for rendering CheckBox component as given below.

{% highlight html %}

 <div>
        Hobbies <br /><br />
        <table>
            <tr>
                <td>
                    <ej-checkbox id="Checkbox1"></ej-checkbox>
                    <label for="Checkbox1">Music</label>
                </td>
                <td>
                    <ej-checkbox id="Checkbox2"> </ej-checkbox>
                    <label for="Checkbox2">Sports</label>
                </td>
                <td>
                    <ej-checkbox id="Checkbox3"> </ej-checkbox>
                    <label for="Checkbox3">Bike Riding</label>
                </td>
            </tr>
        </table><br /><br />
        Favorite Search Engines<br /><br />
        <table>
            <tr>
                <td>
                    <ej-checkbox id="Checkbox4"> </ej-checkbox>
                    <label for="Checkbox4">Google</label>
                </td>
                <td>
                    <ej-checkbox id="Checkbox5"> </ej-checkbox>
                    <label for="Checkbox5">Yahoo</label>
                </td>
                <td>
                    <ej-checkbox id="Checkbox6"> </ej-checkbox>
                    <label for="Checkbox6">Bing</label>
                </td>
            </tr>
        </table>
    </div>

{% endhighlight %} 

3. Create a TypeScript file named "app.ts" file and refer the required definition files as given below.

{% highlight JS %}

        /// <reference path="tsfiles/jquery.d.ts" />
        /// <reference path="tsfiles/ej.web.all.d.ts" />

{% endhighlight %} 

4. Now, initialize the CheckBox component by using ej.CheckBox method. 

{% highlight javascript %}

        /// <reference path="jquery.d.ts" />
        /// <reference path="ej.web.all.d.ts" /> 
        module AppComponent {
            $(function () {
                new ej.CheckBox($("#Checkbox1"), {
                    value: "Music", name: "Hobbies", size: "small",
                    enableTriState: true, checked: true
                });
                new ej.CheckBox($("#Checkbox2"), {
                    value: "sports", name: "Hobbies", size: "small",
                    enableTriState: true, checkState: "indeterminate"
                });
                new ej.CheckBox($("#Checkbox3"), {
                    value: "Bike riding", name: "Hobbies", size: "small",
                    enableTriState: true
                });
                new ej.CheckBox($("#Checkbox4"), {
                    value: "Google", name: "SearchEngines", size: "medium",
                    enableTriState: true, checked: true
                });
                new ej.CheckBox($("#Checkbox5"), {
                    value: "Yahoo", name: "SearchEngines", size: "medium",
                    enableTriState: true, checkState: "indeterminate"
                });
                new ej.CheckBox($("#Checkbox6"), {
                    value: "Bing", name: "SearchEngines", size: "medium",
                    enableTriState: true
                });
            }

{% endhighlight %} 

### Run the application

To run the application, navigate the project folder and open command prompt window and execute the following command.

{% highlight JS %}

tsc

{% endhighlight %} 

This command compiles the app.ts file to generate a JS file named app.js file. 
Refer the app.js file in index.html and browse the html file to see the following output.

![](Getting-Started_images/checkbox.png) 

