---
layout: post
title: Template
description: template
platform: Typescript
control: TreeView
documentation: ug
---


# Template 

Tree nodes can be customized by using [template](https://help.syncfusion.com/api/js/ejtreeview#members:template) property. TreeView template option requires addition JS library called **’JsRender’**, which helps to create the structured way of tree nodes with simple codes and increased performance. To know more about JsRender - [http://www.jsviews.com/](http://www.jsviews.com/#) .  

{% highlight js %}

    <script id="treeTemplate" type="text/x-jsrender">        

      {{"{{"}}if hasChild{{}}}}

         <div class={{"{{"}}>className{{}}}}>{{"{{"}}>name{{}}}}</div>

      {{"{{"}}else{{}}}}

         <div class="cont-list">

            <img class="con-img" src="13.3.0.7/themes/web/images/treeview/template-image-{{"{{"}}>imgId{{}}}}.png" />

            <div class="cont-del"></div>

            <b>{{"{{"}}>name{{}}}}</b><br />

            <span>{{"{{"}}>city{{}}}}</span>

            <br />

            <span>{{"{{"}}>phone{{}}}}</span>

         </div>

         <div class="treeFooter"></div>

         </div>

     {{"{{"}}/if{{}}}}

    </script>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module TreeViewComponent {

       $(function () {

            var treeData = [

            { id: 1, name: "UK", className: "uk-style", hasChild: true, expanded: true },

            { id: 2, pid: 1, imgId: "1", name: "Steven John", city: "London", phone: "555-5665-2323" },

            { id: 3, name: "USA", className: "usa-style", hasChild: true, expanded: true },

            { id: 5, pid: 3, imgId: "3", name: "Andrew", city: "Capital way", phone: "934-8374-2455" },

            { id: 4, pid: 3, imgId: "2", name: "Angelica", city: "Dayton", phone: "988-4243-0806" }

            ];
        var tree = new ej.TreeView($("#treeView"), {

                fields: {

                    dataSource: treeData,

                    id: "id", parentId: "pid", text: "name", hasChild: "hasChild"

                },

                template: "#treeTemplate"

            });

        });

}
{% endhighlight %}

For more details about node template, refer the sample [here](http://jsplayground.syncfusion.com/ncztbhc3#). 