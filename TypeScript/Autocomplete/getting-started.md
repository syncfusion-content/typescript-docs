---
layout: post
title: getting-started
description: getting started
platform: TypeScript
control: AutoComplete
documentation: ug
---

# Getting Started



Using the following steps, you can create a **Typescript** AutoComplete component. The basic rendering of **Typescript** AutoComplete is achieved with default functionality.

## Creating an AutoComplete in Typescript



You can create a **Typescript** application with the help of the given [Typescript Getting Started Documentation. ](https://help.syncfusion.com/js/typescript)

 Within an index.html file and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <title>Typescript Application</title>
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="https://code.jquery.com/jquery-3.0.0.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js" type="text/javascript"></script>

</head>
<body>
    <!--Add AutoComplete here-->
</body>
</html>


{% endhighlight %}



The AutoComplete can be created from a HTML ‘input’ element with the HTML 'id' attribute and pre-defined options set to it. To create the AutoComplete, you should call the `ejAutocomplete` jQuery plug-in function.



{% highlight html %}

    <input id="autocomplete" />
    <script src="app.js"></script>



{% endhighlight %}



Create app.ts file and past the below content



{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TabComponent {
    $(function () {
        let sample = new ej.Autocomplete($("#autocomplete"));
    });
}


{% endhighlight %}



Now build your application, so that the **app.js** file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file automatically.



This will render an Autocomplete with no suggestion on executing.

![](getting-started_images\getting-started_img1.png)

## Data Binding



The data for AutoComplete suggestion list which can be populated using the dataSource property.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TabComponent {
    $(function () {
        let data = [
            { text: "Algeria", sprite: "flag-dz" }, { text: "Argentina", sprite: "flag-ar" },
            { text: "Armenia", sprite: "flag-am" }, { text: "Brazil", sprite: "flag-br" },
            { text: "Bangladesh", sprite: "flag-bd" }, { text: "Canada", sprite: "flag-ca" },
            { text: "Cuba", sprite: "flag-cu" }, { text: "China", sprite: "flag-cn" },
            { text: "Denmark", sprite: "flag-dk" }, { text: "Estonia", sprite: "flag-ee" },
            { text: "Egypt", sprite: "flag-eg" }, { text: "France", sprite: "flag-fr" },
            { text: "Finland", sprite: "flag-fi" }, { text: "Greenland", sprite: "flag-gl" },
            { text: "India", sprite: "flag-in" }, { text: "Indonesia", sprite: "flag-id" },
            { text: "Malaysia", sprite: "flag-my" }, { text: "Mexico", sprite: "flag-mx" },
            { text: "New Zealand", sprite: "flag-nz" }, { text: "Netherlands", sprite: "flag-nl" },
            { text: "Norway", sprite: "flag-no" }, { text: "Portugal", sprite: "flag-pt" },
            { text: "Poland", sprite: "flag-pl" }, { text: "Qatar", sprite: "flag-qa" },
            { text: "Romania", sprite: "flag-ro" }, { text: "Spain", sprite: "flag-es" },
            { text: "Singapore", sprite: "flag-sg" }, { text: "Saudi Arabia", sprite: "flag-sa" },
            { text: "Thailand", sprite: "flag-th" }, { text: "Turkey", sprite: "flag-tr" },
            { text: "Ukraine", sprite: "flag-ua" }, { text: "United States", sprite: "flag-us" },
            { text: "Uruguay", sprite: "flag-uy" }, { text: "Viet Nam", sprite: "flag-vn" },
            { text: "Yemen", sprite: "flag-ye" }
        ];

        let sample = new ej.Autocomplete($("#autocomplete"), {watermarkText:"Select a country", dataSource: data, fields: { text: "text", key: "sprite" } }); 
    });
}


{% endhighlight %}



Run the above code to render the following output:



![](getting-started_images\getting-started_img2.png)

## Enable Popup Button



We can enable the popup button of AutoComplete by using showPopupButton property which helps you to show all the available suggestions on clicking it.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module TabComponent {
    $(function () {
        let data = [
            { text: "Algeria", sprite: "flag-dz" }, { text: "Argentina", sprite: "flag-ar" },
            { text: "Armenia", sprite: "flag-am" }, { text: "Brazil", sprite: "flag-br" },
            { text: "Bangladesh", sprite: "flag-bd" }, { text: "Canada", sprite: "flag-ca" },
            { text: "Cuba", sprite: "flag-cu" }, { text: "China", sprite: "flag-cn" },
            { text: "Denmark", sprite: "flag-dk" }, { text: "Estonia", sprite: "flag-ee" },
            { text: "Egypt", sprite: "flag-eg" }, { text: "France", sprite: "flag-fr" },
            { text: "Finland", sprite: "flag-fi" }, { text: "Greenland", sprite: "flag-gl" },
            { text: "India", sprite: "flag-in" }, { text: "Indonesia", sprite: "flag-id" },
            { text: "Malaysia", sprite: "flag-my" }, { text: "Mexico", sprite: "flag-mx" },
            { text: "New Zealand", sprite: "flag-nz" }, { text: "Netherlands", sprite: "flag-nl" },
            { text: "Norway", sprite: "flag-no" }, { text: "Portugal", sprite: "flag-pt" },
            { text: "Poland", sprite: "flag-pl" }, { text: "Qatar", sprite: "flag-qa" },
            { text: "Romania", sprite: "flag-ro" }, { text: "Spain", sprite: "flag-es" },
            { text: "Singapore", sprite: "flag-sg" }, { text: "Saudi Arabia", sprite: "flag-sa" },
            { text: "Thailand", sprite: "flag-th" }, { text: "Turkey", sprite: "flag-tr" },
            { text: "Ukraine", sprite: "flag-ua" }, { text: "United States", sprite: "flag-us" },
            { text: "Uruguay", sprite: "flag-uy" }, { text: "Viet Nam", sprite: "flag-vn" },
            { text: "Yemen", sprite: "flag-ye" }
        ];

let sample = new ej.Autocomplete($("#autocomplete"), {showPopupButton:true, watermarkText:"Select a country", dataSource: data, fields: { text: "text", key: "sprite" } });
    });
}


{% endhighlight %}



Run the above code to render the following output:



![](getting-started_images\getting-started_img3.png)



> _Note: You can find the Autocomplete properties from the_ [API reference](https://help.syncfusion.com/api/js/ejautocomplete) _document_







