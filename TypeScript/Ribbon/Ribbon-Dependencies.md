---
layout: post
title: Ribbon-Dependencies
description: ribbon dependencies
platform: Typescript
control: Ribbon
documentation: ug
---

# Ribbon Dependencies

**ej.web.all.js** is a bundle of all Essential JavaScript controls. When you use ej.web.all.js in your application, you can leave this section or else you can try to render ej ribbon in your application by using ej.ribbon file. You can refer to the following frameworks and controls in your project.

<table>
   <tr>
      <th>
         <b>Files</b>
      </th>
      <th>
         <b>Description/Usage </b>
      </th>
   </tr>
   <tr>
      <td>
         ej.core.min.js
      </td>
      <td>
         Must always be referred to before using all the <i><b>JS</b></i> controls.
      </td>
   </tr>
   <tr>
      <td>
         ej.data.min.js
      </td>
      <td>
         Used to handle data manger operation and should be used while binding data to <i><b>JS</b></i> controls.
      </td>
   </tr>
   <tr>
      <td>
        ej.globalize.min.js
      </td>
      <td>
        Must be referred to localize any of the JS control's text and content.
      </td>
   </tr>
   <tr>
      <td>
         ej.ribbon.min.js
      </td>
      <td>
         Should be referred when using <i><b>Ribbon</b></i><b> </b>control.
      </td>
   </tr>
   <tr>
      <td>
         ej.waitingpopup.min.js
      </td>
      <td>
        This file is used to render waiting popup when on-demand functionality is enabled in ribbon.
      </td>
   </tr>
   <tr>
      <td>
         ej.menu.min.js
      </td>
      <td>
         This file is used to render menu in the application tab.
      </td>
   </tr>
   <tr>
      <td>
         ej.scroller.min.js
      </td>
      <td>
         This file is used to render scroller in the Ribbon control.
      </td>
   </tr>
   <tr>
      <td>
         ej.checkbox.min.js
      </td>
      <td>
         This file is used to render checkboxes in the Ribbon control.
      </td>
   </tr>
   <tr>
      <td>
         ej.tab.min.js
      </td>
      <td>
         This file is used to render tabs into the Ribbon control.
      </td>
   </tr>
   <tr>
      <td>
         ej.dropdownlist.min.js
      </td>
      <td rowspan = "4">
         These files are used to render button,split button,toggle button, and dropdown list controls in the ribbon groups.
      </td>
   </tr>
   <tr>
      <td>
         ej.splitbutton.min.js
      </td>
   </tr>
   <tr>
      <td>
         ej.button.min.js
      </td>
   </tr>
   <tr>
      <td>
         ej.togglebutton.min.js
      </td>
   </tr>
</table>