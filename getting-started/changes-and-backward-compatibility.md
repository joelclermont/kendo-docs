---
title: Changes and Backward Compatibility
slug: gs-changes-and-backward-compatibility
publish: true
---

# Kendo UI Framework Changes and Backwards Compatibility

## KendoUI 2012 Q2

### Changes from 2011 Q1 SP1 (2011.1.515)

#### Breaking changes

*  **All Widgets:** All arrows have been renamed to better reflect their direction and size. For instance:

    - Old

            .k-arrow-up
            .k-arrow-next
            .k-arrow-down
            .k-arrow-prev
            .k-arrow-first
            .k-arrow-last

    - New

            .k-i-arrow-n
            .k-i-arrow-e
            .k-i-arrow-s
            .k-i-arrow-w
            .k-i-seek-w
            .k-i-seek-e
    for more information check the [Styling Icons demo](http://demos.kendoui.com/web/styling/icons.html).

*  **Popup:** Popup based widgets nested in other Popup based widgets create their Popup container inside the Popup parent. This means that a DropDownList created inside an already
    initialized Menu will create its list inside the Menu item's parent Popup.
*  **TreeView:** The TreeView widget now depends on kendo.data.js
*  **TreeView:** Using the API methods will re-create the HTML of the nodes. In order to get the new reference to the nodes, use the return value of the methods.

    - Old

            var foo = treeviewObject.findByText("foo");
            treeviewObject.append(foo);
            // starting with 2012 Q2, foo will point to a DOM node that is removed from the document
            foo.text("bar: foo");

    - New

            var foo = treeviewObject.findByText("foo");
            foo = treeviewObject.append(foo);
            foo.text("bar: foo");

## KendoUI 2012 Q1 (2012.1.322)

### Changes from 2011 Q3 SP1 (2011.3.1407)

#### Breaking changes

> The combined JavaScript file kendo.all.js is available only in the Kendo Complete package. The corresponding file in Kendo Web is called kendo.web.js. Use it instead of kendo.all.js.

*  **Data:** kendo.model.js file has been removed. The content of kendo.model.js file has been consolidated with the kendo.data.js content.
*  **Data:** `Model.id` is no longer a function. It is a field.
    - Old

            var model = dataSource.get(42);
            var modelId = model.id(); //42
    - New

            var model = dataSource.get(42);
            var modelId = model.id; //42

*  **Data:** The `DataSource` contains ObservableObject instances instead of raw JavaScript objects.

*  **Grid:** The Grid widget is now using the `uid` field of the Model instead of the `id`. A new uid field is introduced to the DataSource's Model,
    which represents its unique id. The Grid row data attribute has been changed to use this field.
    Note that in order to retrieve Model instance by its uid, DataSource's `getByUid` method should be used.
    - Old

            <tr data-id="42"><!--...--></tr>
    - New

            <tr data-uid=”aaaaa-bbbbb-ddddd-gggg”><!--...--></tr>

*  **DataViz:** The kendo.chart(.min).js file is replaced by kendo.dataviz(.min).js
*  **DataViz:** The axis orientation property deprecated in favor of dedicated verticalLine and verticalArea chart types
*  **DataViz:** The suite now requires kendo.dataviz.css to be included
*  **DataViz:** The Chart widget is now in the kendo.dataviz.ui namespace. Previously it was part of kendo.ui
*  **Other:** `dataValueField` and `dataTextField` of DropDownList, ComboBox and AutoComplete, are set to empty string by default. In order to get your old code working, you will need to list the fields manually, like this:
    - Old

            $("#combobox").kendoComboBox([
                {text: "Item 1", value: "item1"},
                {text: "Item 2", value: "item2"}
            ]);
    - New

            $("#combobox").kendoComboBox({
                dataTextField: "text",
                dataValueField: "value",
                dataSource: [
                    {text: "Item 1", value: "item1"},
                    {text: "Item 2", value: "item2"}
                ]
            });
