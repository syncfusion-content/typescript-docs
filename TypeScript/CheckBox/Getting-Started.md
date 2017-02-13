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

* Create a TypeScript application and refer the dependent modules, script and CSS with the help of given [getting started document](https://help.syncfusion.com/js/typescript).

* In the index.HTML file, add the input element for rendering CheckBox component as given below.

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

* Create app.ts file and use the below content

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

Now build your application, so that the app.ts file will compiled and automtically generated the app.js file which is added to your project (User have nothing to do with this file). Now, whatever code changes that you make in app.ts file will be reflected in app.js file by compiling build the aplication.

Execution of above code will render the following output.

![](Getting-Started_images/checkbox.png) 

