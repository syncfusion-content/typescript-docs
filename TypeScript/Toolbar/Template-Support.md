---
layout: post
title: Template-Support
description: template support
platform: TypeScript
control: Toolbar
documentation: ug
---

# Template Support

Template allows you to insert custom controls inside the toolbar items. Also you can design simple drop down buttons listing the items and radio button inside the **Toolbar**.

Set the list for **DropDown control** inside a list tag and define this tag as a **Toolbar** item. You can use all simple controls as a **Toolbar** item. To add RadioButton and DropDownList to **Toolbar**, use the following code example.

{% highlight html %}

<div id="toolbar">
   <ul>
      <li>
         <div>
            <input type="radio" name="small" id="Radio1" />
         </div>
         Option 1
      </li>
      <li id="Dropdown" title="Dropdown Control">
         <input id="selectcar" type="text" />
        
      </li>
   </ul>
</div>

{% endhighlight %}

{% highlight js %}

/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module ToolbarComponent {
    
    $(function () {
        // declaration
          var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
        var sample1 = new ej.RadioButton($("#Radio1"),{     
            size:"medium"
            });
        var sample2 = new ej.DropDownList($("#selectcar"),{       
             dataSource: skills,
              fields: { text: "skill" },
              watermarkText: "Select your skill"
              });
        var sample3 = new ej.ejToolbar($("#toolbar"),{      
             width: "250px", 
             height: "28px" 
        });
    });

}
{% endhighlight %}


##Through Items API:

{% highlight html %}

    <div id="toolbar"></div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        
          var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
        var ToolbarInstance = new ej.Toolbar($("#toolbar"),{
			 Items:[
                    {id:"item1",group:"group1",template:"<input type='radio' id='Radio1' name='radio'>Option 1</input>"},
					{id: "item2",group:"group2",template:"<input type='text' id='dropdown1' />"}
					],
           });
             var RadioInstance = new ej.DropDownList($("#Radio1"),{
                   size:"medium"
                 });
                var DropDownListInstance = new ej.DropDownList($("#dropdown1"),{ 
                dataSource: skills,
                fields: { text: "skill" },
                watermarkText: "Select your skill",
               
            });
    });


{% endhighlight %}

##Through template field in dataSource API:

{% highlight html %}

    <div id="toolbar"></div>

{% endhighlight %}

{% highlight js %}

    $(function () {
      var skills = [
                { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
                { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
                { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
                { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
            ];
     toolbaritems = [
		  {
               id: "1",
               title:"radio",
			   template:"<input type='radio' id='radio1'>Option 1</input>",
			   groups:"group1"

            },
			 {
			         id:"2",
					 title:"dropdown",
					 template:"<input type='text' id='dropdown2'></div>",
					 group:"group2"
			 }],
        var sample = new ej.Toolbar($("#toolbar"),{
			  dataSource: toolbaritems,
              fields: { id: "id",tooltipText:"title",group:"group",template:"template"},

             
			  });
        var sample1 = new ej.RadioButton($("#radio1"),{     
                  size:"medium"
            });
        var sample2 = new ej.DropDownList($("#dropdown2"),{         
                dataSource: skills,
                fields: { text: "skill" },
                watermarkText: "Select your skill",
              });
    });


{% endhighlight %}

The following screenshot displays a Toolbar with embedded controls.

![](Template-Support_images/Template.JPG)
