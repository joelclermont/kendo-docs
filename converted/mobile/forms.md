---
title: Forms
publish: true
---

Kendo UI Mobile provides automatic platform dependent styling of form elements when they are added to a mobile View. Currently the following form elements are supported and styled:

*   Inputs of types **text**, **password**, **search**, **url**, **email**, **number**, **tel**, **file**(not in iOS), **date**, **time** **month** and **datetime**;
*   Single **select** elements or Kendo DropDownList replacements. 

The input elements with a picker use the native one from the current platform if it is supported.
HTML5 form elements are fully functional only on the following platforms: iOS 5.x+, Android 4.x+, BlackBerry 6.x+, BlackBerry Playbook 1.x+.
The styling will still work on older platforms, but the functionality will be limited to text input only.

Select elements are also automatically styled for each platform and will use the native select dialog or popup.

Known browser issues and possible workarounds:

*   Select element touch target in Android 2.x remains in the same place when a transformation is applied on a parent.
Select element text can't be right-aligned in WebKit, which is needed for iOS styling.
A work around for both is to use the Kendo DropDownList widget.
It receives platform specific styling when initialized in a Kendo UI Mobile application.
To do so, include **kendo.dropdownlist.js** and its requirements
**kendo.list.js** and **kendo.popup.js** in the application.

*   Input with type search shows **reset icon** in Chrome and Safari, which is not present on a mobile device.
*   All input and select elements in Android 4.x default browser render a fake input when focused.
This focused input can't be styled and is not part of the page flow so it won't scroll
resulting in 2 identical but differently styled input elements at some point.
There is no workaround for this issue, unless the form fits the screen and no scrolling is needed.
*   Select element drop down arrow can't be removed in Firefox.