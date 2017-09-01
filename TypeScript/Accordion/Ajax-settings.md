---
layout: post
title: Ajax-settings
description: ajax settings
platform: Typescript
control: Accordion 
documentation: ug
---

# AJAX settings

**Accordion** widgets allow you to load content for the **Accordion** panel using **AJAX**. This renders content from the specified **URL** location that is set to the anchor tag. You can set the destination file URL string by using **ajaxUrl** property **AJAX** contents enables you to load the content of the **Accordion** panel when it is expanded. This enhances the **Accordion** control efficiency when a large content is to be loaded into the panel.

## Populate accordion with AJAX content

* Create HTML files with required content to be loaded for Accordion panel and save it in your drive location.
* In the HTML page, define a div element that is a container for Accordion widget and add the contents URL location in the &lt;a&gt; tag accordingly.

{% highlight html %}

<div id="ajaxAccordion" style="width: 650px">
   <h3>
      <a href="mvccontent.html">Model–view–controller (MVC)</a>
   </h3>
   <div>
   </div>
   <h3>
      <a href="wpfcontent.html"></a>WPF
   </h3>
   <div>
   </div>
   <h3>
      <a href="#">WCF</a>
   </h3>
   <div>
      <p>
         WCF is a tool often used to implement and deploy a service-oriented architecture (SOA). 
         It is designed using service-oriented architecture principles to support distributed computing where services have remote consumers. 
         Clients can consume multiple services; services can be consumed by multiple clients. Services are loosely coupled to each other. 
         Services typically have a WSDL interface (Web Services Description Language) that any WCF client can use to consume the service, regardless of which platform the service is hosted on. 
         WCF implements many advanced Web services (WS) standards such as WS-Addressing, WS-ReliableMessaging and WS-Security. 
         With the release of .NET Framework 4.0, WCF also provides RSS Syndication Services, WS-Discovery, routing and better support for REST services.
      </p>
   </div>
</div>
{% endhighlight %}

{% highlight javascript %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module AccordionComponent {
    $(function () {
        var sample = new ej.Accordion($("#ajaxAccordion"), {
        });
    });
}

{% endhighlight %}

Output for Accordion control with loaded AJAX content is as follows.



![](Ajax-settings_images/Ajax-settings_img1.png)

