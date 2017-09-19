---
layout: post
title: Localization in DropDownList widget
description: Localization in DropDownList widget
platform: Typescript
control: DropDownList
documentation: ug
keywords: Localization, DropDownList, dropdown
---
# Localization

The DropDownList provides option to localize its strings, it is used to adapting the DropDownList to a particular local language. By default, the DropDownList will use the US English (en-US) as its language.

N> The culture name has to be specified in a standard format such as [Language Code]-[County/Region Code].

To localize the dropdownlist’s strings with your own localization, copy the default language informations and localize the strings in the values column. For example, to localize the DropDownList in German language (“de-DE”).

Set the locale property of the DropDownList to the new language.


{% highlight javascript %}

    <input type="text" id="selectCompany" />
/// <reference path="tsfiles/jquery.d.ts" />
/// <reference path="tsfiles/ej.web.all.d.ts" />

module DropDownListComponent {
    $(function () {
        var dataList = ej.DataManager({ url: "http://mvc.syncfusion.com/services/Northwnd.svc/Customers" });
        var sample = new ej.DropDownList($("#selectCompany"),{
            dataSource: dataList,
            fields: { text: "CompanyName", value: 'ContactName' },
            width: 260,
            showCheckbox: true,
            locale: "de-DE",
            enableFilterSearch: true,
            enablePopupResize: true

        });

    });
    ej.DropDownList.Locale["de-DE"] = {
        emptyResultText: "Keine Vorschläge" //replace with your text  
    };
}  
{% endhighlight %}
