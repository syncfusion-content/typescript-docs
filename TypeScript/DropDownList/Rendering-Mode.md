---
layout: post
title: Rendering Mode in DropDownList widget
description: Describes about rendering mode in DropDownList widget 
platform: Typescript
control: DropDownList
documentation: ug
keywords: Rendering, DropDownList, dropdown, Rendering Mode
---

# Rendering Mode

DropDownList widget can be created in three ways.

*  Using an input element 
*  Using a select element 
*  Using UL-LI 

## Using an input element

Create an input element with the HTML "id" attribute set to it. To initialize the DropDownList, you should call the "ejDropDownList" jQuery plug-in function with the options as parameter

You can bind the local JSON array data source to the DropDownList using [dataSource](https://help.syncfusion.com/api/js/ejdropdownlist#members:datasource) and [fields](https://help.syncfusion.com/api/js/ejdropdownlist#members:fields) properties. Fields property is used to map with the corresponding columns.

{% highlight html %}

	<input type="text" id="dropdown1" />

{% endhighlight %}


{% highlight javascript %}
	
	
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {

			var items = [{ text: "ListItem 1", value: "item1" },
			
				{ text: "ListItem 2", value: "item2" },
			
				{ text: "ListItem 3", value: "item3" },
			
				{ text: "ListItem 4", value: "item4" },
			
				{ text: "ListItem 5", value: "item5" }];
			
    $(function () {
        var sample = new ej.DropDownList($("#dropdown1"),{
			
				dataSource: items,
			
				fields: { text: "text", value: "value" }
			
			});
		
		});	

}
{% endhighlight %}

## Using Select Element

You can create a DropDownList using a select element and the detailed information is given in [creating DropDownList](getting-started#creating-dropdownlist) section.

## Using UL-LI

You can bind the predefined set of UL-LI elements to generate the list of popup items. These items can be customized by adding any images, div elements, radio buttons, text boxes etc.

Create a div with UL-LI elements and assign that div id into [targetID](https://help.syncfusion.com/api/js/ejdropdownlist#members:targetid ) property and initialize the widget.

{% highlight html %}

	<input type="text" id="dropdown1" />

	<div id="tools">

    	<ul>

        	<li>

            	<div class="mailtools categorize"></div>
            	Categorize and Move</li>
        
        	<li>
            	<div class="mailtools done"></div>
            	Done</li>
        
        	<li>
            
            	<div class="mailtools flag"></div>
            	Flag & Move</li>
        
        	<li>
            
	            <div class="mailtools forward"></div>
    	        Forward</li>
        
	        <li>
            
	            <div class="mailtools movetofolder"></div>
	            Move to Folder</li>
        
	        <li>
            
	            <div class="mailtools newmail"></div>
	            New E-mail</li>
        
	        <li>
            
	            <div class="mailtools meeting"></div>
	            New Meeting</li>
        
	        <li>
            
	            <div class="mailtools reply"></div>
	            Reply & Delete</li>
        
    	</ul>
    
	</div>
	
{% endhighlight %}

{% highlight css %}

    	 .mailtools {
        	display: block;
        	background-image: url('iconsapps.png');
        	height: 25px;
        	width: 25px;
        	background-position: center center;
        	background-repeat: no-repeat;
        
    	}
    
     	.mailtools.done {
	        background-position: 0 0;
        
	    }
    
	     .mailtools.movetofolder {
    	    background-position: 0 -22px;
        
	    }
    
	     .mailtools.categorize {
	        background-position: 0 -46px;
        
	    }
    
	    .mailtools.flag {
    	    background-position: 0 -70px;
        
    	}
    
     	.mailtools.forward {
        	background-position: 0 -94px;
        
    	}
    
     	.mailtools.newmail {
        	background-position: 0 -116px;
        
	    }
    
    	 .mailtools.reply {
        	background-position: 0 -140px;
        
    	}
    
     	.mailtools.meeting {
        	background-position: 0 -164px;
        
    	}    

{% endhighlight %}

{% highlight javascript %}

/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
    	$(function() {
		
        	 var sample = new ej.DropDownList($("#dropdown1"),{
			
            	targetID: "tools"
				
        	});
			
    	});
 }	

{% endhighlight %}


N> Images for this sample are available in (installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\samples\web\themes\images<br/>
	
	
![](RenderingMode_images/RenderingMode_img1.jpeg)

N> Any EJ widget can be embedded in the target element but the default action of that widget should be prevented in order to create custom actions. To show a sample, integration with [TreeView](https://help.syncfusion.com/api/js/ejtreeview) widget is demonstrated [here](http://jsplayground.syncfusion.com/Sync_t4ife2xh).
