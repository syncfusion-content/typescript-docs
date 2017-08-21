---
layout: post
title: Sorting
description: sorting support
platform: typescript
control: ListBox
documentation: ug
---

# Sorting

 We can change ListBox items rendering order either as ascending or descending, by using [ej.SortOrder](https://help.syncfusion.com/api/js/ejlistbox#members:sortorder) property. By default ej.SortOrder will be "None". Please use code as like in below,

 {% tabs %} 
 {% highlight html %}

     <div class="contents">
          <ul id="selectsection"></ul> 
    </div>

 {% endhighlight %}

 {% highlight javascript %}

<script type="text/javascript">

 /// <reference path="tsfiles/jquery.d.ts" />
 /// <reference path="tsfiles/ej.web.all.d.ts" />\

module ListBoxComponent {
        $(function () {
            var skills = [{ skill: "F#" }, { skill: "ActionScript" }, { skill: "Delphi" }, { skill: "Basic" },
            { skill: "C++" }, { skill: "ESPOL" }, { skill: "C#" }, { skill: "DBase" }, { skill: "ASP.NET" }
            ];
    var listboxInstance = new ej.ListBox($("#selectsection"), {
                width: "220", dataSource: skills,
                fields: { text: "skill" },
                sortOrder:ej.SortOrder.Descending
                 })
            });
}
 </script>

  {% endhighlight %}
{% endtabs %} 
  
  ![](Sorting_Images\Sorting_img1.png)
   

