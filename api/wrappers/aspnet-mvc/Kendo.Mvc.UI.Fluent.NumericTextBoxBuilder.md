---
title:Kendo.Mvc.UI.Fluent.NumericTextBoxBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxBuilder

## Methods

### 1.Value(System.Nullable{`0})
Sets the initial value of the NumericTextBox.

### 1.Step(`0)
Sets the step, used ti increment/decrement the value of the textbox.

### 1.Min(System.Nullable{`0})
Sets the minimal possible value allowed to the user.

### 1.Max(System.Nullable{`0})
Sets the maximal possible value allowed to the user.

### 1.Placeholder(System.String)
Sets the text which will be displayed if the textbox is empty.

### 1.Spinners(System.Boolean)
Enables or disables the spin buttons.

#### Parameters

##### allowSpinner `System.Boolean`

            

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        .Events(events =>
        events.OnLoad("onLoad").OnChange("onChange")
        )
        %>

#### Parameters

##### EventsAction `System.Action{Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder}`
The client events action.

### 1.Enable(System.Boolean)
Enables or disables the textbox.

#### Parameters

##### allowSpinner `System.Boolean`

            

### 1.Format(System.String)
Stes the format of the NumericTextBox.

#### Parameters

##### allowSpinner `System.String`

            