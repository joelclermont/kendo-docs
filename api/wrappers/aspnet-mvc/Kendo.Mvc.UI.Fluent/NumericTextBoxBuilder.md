---
title:NumericTextBoxBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxBuilder

Defines the fluent interface for configuring the NumericTextBox component.

## Methods

### Value(System.Nullable<T>)
Sets the initial value of the NumericTextBox.

### Step(<T>)
Sets the step, used ti increment/decrement the value of the textbox.

### Min(System.Nullable<T>)
Sets the minimal possible value allowed to the user.

### Max(System.Nullable<T>)
Sets the maximal possible value allowed to the user.

### Placeholder(System.String)
Sets the text which will be displayed if the textbox is empty.

### Spinners(System.Boolean)
Enables or disables the spin buttons.

#### Parameters

##### allowSpinner `System.Boolean`

### Events(System.Action<Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder>)
Configures the client-side events.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events =>
        events.OnLoad("onLoad").OnChange("onChange")
        )
        %>

#### Parameters

##### EventsAction System.Action<[Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder>](/api/wrappers/aspnet-mvc/Kendo.Mvc.UI.Fluent/NumericTextBoxEventBuilder>)>
The client events action.

### Enable(System.Boolean)
Enables or disables the textbox.

#### Parameters

##### allowSpinner `System.Boolean`

### Format(System.String)
Stes the format of the NumericTextBox.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Format("c3")
        %>

### Culture(System.String)
Specifies the culture info used by the NumericTextBox widget.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Culture("de-DE")
        %>

### Decimals(System.Int32)
Specifies the number precision. If not set precision defined by current culture is used.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Decimals(3)
        %>