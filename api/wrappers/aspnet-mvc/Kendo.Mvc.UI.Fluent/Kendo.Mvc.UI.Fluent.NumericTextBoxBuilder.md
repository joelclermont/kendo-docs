---
title:Kendo.Mvc.UI.Fluent.NumericTextBoxBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.numerictextboxbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NumericTextBoxBuilder

## Methods

### Value(System.Nullable{`0})
Sets the initial value of the NumericTextBox.

### Step(`0)
Sets the step, used ti increment/decrement the value of the textbox.

### Min(System.Nullable{`0})
Sets the minimal possible value allowed to the user.

### Max(System.Nullable{`0})
Sets the maximal possible value allowed to the user.

### Placeholder(System.String)
Sets the text which will be displayed if the textbox is empty.

### Spinners(System.Boolean)
Enables or disables the spin buttons.

#### Parameters

##### allowSpinner `System.Boolean`

            

### Events(System.Action{Kendo.Mvc.UI.Fluent.NumericTextBoxEventBuilder})
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

### Enable(System.Boolean)
Enables or disables the textbox.

#### Parameters

##### allowSpinner `System.Boolean`

            

### Format(System.String)
Stes the format of the NumericTextBox.

#### Parameters

##### allowSpinner `System.String`

            