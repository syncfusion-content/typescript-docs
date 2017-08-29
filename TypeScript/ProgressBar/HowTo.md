---
layout: post
title: How to - ProgressBar widget
description: How To Section in ProgressBar widget
platform: TypeScript
control: ProgressBar
documentation: ug
keywords: ProgressBar, events
---

# How To

## How to increment & show the progressbar movement

You can increment the progress percentage and show case the movement by using the below code

{% highlight html %}

        <div class="frame">
            <div class="control">
                <div id="progressBar"></div>
            </div>
            <div class="startButton">
                <input type="checkbox" id="startButton" />
                 <label for="startButton">Toggle</label>
            </div>
        </div>  
         <div class="cols-prop-area event-tracer">
                    <div class="heading">
                        <span>Event Trace</span>
                        <div class="pull-right">
                            <select name="selectevtprops" id="selectControls">
                                <option value="start">start</option>
                                <option value="complete">complete</option>
                                <option value="change">change</option>
                            </select>
                        </div>
                    </div>
					<div class="prop-grid content">
						<div class="eventarea">
							<div class="EventLog" id="EventLog">
							</div>
						</div>
						<div class="evtbtn">
							<input type="button" class="eventclear e-btn" value="Clear" onclick="onClear()" />
						</div>
					</div>    
            </div> 
     
{% endhighlight %}

{% highlight javascript %}

       var , k = 10, timer = window.clearInterval(timer),showComplete=true ;
/// <reference path="../tsfiles/jquery.d.ts" />
/// <reference path="../tsfiles/ej.web.all.d.ts" />

module ProgressBarComponent {
    $(function () {
        var sample = new ej.ProgressBar($("#progressBar"),{
                height: 22,
                value: 10,
                start: "onstart",
                change: "onchange",
                complete: "completed"
            });
            sample.option("text", progresObj.getPercentage() + " %");

      var sample1 = new ej.ToggleButton($("#startButton"),{
                defaultText: "Start",
                activeText: "Pause",
                size: "small",
                click: "startProcess"
            });
     var sample2 = new ej.DropDownList($("#selectControls"),{
                popupShown: "adjustpopupposition",
                showCheckbox: true,
                checkAll: true,
                change: "evtpropscheckedevent"
            });
        });

        function evtpropscheckedevent(args) {
            if (args.isChecked) {
                switch (args.value) {
                    case "start": sample.option(args.value, "onstart"); break;
                    case "change": sample.option(args.value, "onchange"); break;
                    case "complete": showComplete=true; break;
                }
            }
            else if(args.value=="complete") 
			{             
                 showComplete=false; 
            }
            else
			   sample.option(args.value, null)            
        }

        function startProcess(args) {
            if (args.isChecked) 
                timer = window.setInterval(draw, 100);
            else {
                sample1.setModel({ "defaultText": "Start" });
                timer = window.clearInterval(timer);
            }
        }
        function draw() {
            sample.option("text", ++k + " %");
            sample.option("percentage", k);
        }
        function completed(args) {
            sample.option("text", "Completed");
            timer = window.clearInterval(timer);
            k = 0;
            if(showComplete)
            oncomplete(args);
            sample1.setModel({ "toggleState": false, "defaultText": "Restart" });
        }

        function oncomplete(args) {
                jQuery.addEventLog("The process has been <span class='eventTitle'>completed</span> successfully.</br>");
        }
        function onstart(args) {
            jQuery.addEventLog("Progressbar has been <span class='eventTitle'>started</span>.</br>");
        }
        function onchange(args) {
            jQuery.addEventLog("Progressbar value has been <span class='eventTitle'>changed</span> to " + args.percentage + "%.</br>");
        }
        function onClear() {
            $("#EventLog").html("");
        }
    
 
{% endhighlight %}

{% highlight css %}

     <style type="text/css" class="cssStyles">
        .frame {
            border: 1px solid #BBBCBB;
            border-radius: 10px 10px 10px 10px;
            padding: 50px 60px;
            margin-top: 40px;
            width: 400px;
            }
       
        .txt {
           font-size: 20px;
           margin-top: 12px;
           text-align: center;
           }
        .startButton {
             margin-left: 155px;
           }
    </style>

{% endhighlight %}

The progress bar movement will be as shown below:

![](HowTo_images/HowTo_img1.jpeg)

![](HowTo_images/HowTo_img2.jpeg)


