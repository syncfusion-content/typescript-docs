---
layout: post
title: getting-started
description: getting started
platform: Typescript
control: ListView
documentation: ug
---

# Getting Started

 Using the following steps, you can create a **Typescript** ListView component. The basic rendering of **Typescript** ListView is achieved with default functionality.

## Create a ListView


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
    <!--Add ListView here-->
</body>
</html>


{% endhighlight %}



Add a **&lt;div&gt;** element. It is a container for **ListView** control. To create the **ListView**, you should call the `ejListView` jQuery plug-in function.

{% highlight html %}

<div id="listview">
        <ul>
            <li data-ej-text="Inbox"></li>
            <li data-ej-text="VIP"></li>
            <li data-ej-text="Drafts"></li>
            <li data-ej-text="Sent"></li>
            <li data-ej-text="Junk"></li>
            <li data-ej-text="All mails"></li>
            <li data-ej-text="Mail"></li>
        </ul>
    </div>
<script src="app.js"></script>



{% endhighlight %}



Initialize the ListView in app.ts file by using the ej.ListView method.

{% highlight js %}

/// <reference path="jquery.d.ts" />  
/// <reference path="ej.web.all.d.ts" />

module ListComponent {
    $(function () {
        var sample = new ej.ListView($("#listview”"), {
            
    });
}


{% endhighlight %}



Now build your application, so that the **app.js** file is automatically generated and got added to your project (User have nothing to do with this file). Now, whatever code changes that you make in **app.ts** file will be reflected in app.js file automatically.

Run the above code to render the following output:

![](getting-started_images\getting-started_img1.png)



## Add Header

You can add a header for **ListView**. Refer to the following script.

{% highlight js %}

  module ListComponent {
        $(function () {
            let sample = new ej.ListView($("#listview"),{showHeader: true, headerTitle: "Mailbox"});
            });
    }


{% endhighlight %}





Run the above code to render the following output:

![](getting-started_images\getting-started_img2.png)



> _Note: You can find the ListView properties from the_ [API reference](https://help.syncfusion.com/api/js/ejlistview) document

