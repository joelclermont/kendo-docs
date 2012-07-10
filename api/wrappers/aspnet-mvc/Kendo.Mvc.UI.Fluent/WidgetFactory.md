---
title:WidgetFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.widgetfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.WidgetFactory

Creates the fluent API builders of the Kendo UI widgets

## Methods

### Menu
Creates a Menu

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => { /* add items here */ });
        %>

### Editor
Creates a Editor

#### Example
    <%= Html.Kendo().Editor()
        .Name("Editor");
        %>

### Grid`
Creates a new !:Grid<T> bound to the specified data item type.

#### Example
    <%= Html.Kendo().Grid<Order>()
        .Name("Grid")
        .BindTo(Model)
        %>

### Grid`(System.Collections.Generic.IEnumerable{``0})
Creates a new !:Kendo.Web.UI.Grid<T> bound to the specified data source.

#### Example
    <%= Html.Kendo().Grid(Model)
        .Name("Grid")
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

### Grid(System.Data.DataTable)
Creates a new !:Kendo.Web.UI.Grid<T> bound to a DataTable.

#### Parameters

##### dataSource `System.Data.DataTable`
DataTable from which the grid instance will be bound

### Grid(System.Data.DataView)
Creates a new !:Kendo.Web.UI.Grid<T> bound to a DataView.

#### Parameters

##### dataSource `System.Data.DataView`
DataView from which the grid instance will be bound

### Grid`(System.String)
Creates a new !:Kendo.Web.UI.Grid<T> bound an item in ViewData.

#### Example
    <%= Html.Kendo().Grid<Order>("orders")
        .Name("Grid")
        %>

#### Parameters

##### dataSourceViewDataKey `System.String`
The data source view data key.

### ListView`
Creates a new !:ListView<T> bound to the specified data item type.

#### Example
    <%= Html.Kendo().ListView<Order>()
        .Name("ListView")
        .BindTo(Model)
        %>

### ListView`(System.Collections.Generic.IEnumerable{``0})
Creates a new !:Kendo.Web.UI.ListView<T> bound to the specified data source.

#### Example
    <%= Html.Kendo().ListView(Model)
        .Name("ListView")
        %>

#### Parameters

##### dataSource `System.Collections.Generic.IEnumerable{``0}`
The data source.

### ListView`(System.String)
Creates a new !:Kendo.Web.UI.ListView<T> bound an item in ViewData.

#### Example
    <%= Html.Kendo().ListView<Order>("orders")
        .Name("ListView")
        %>

#### Parameters

##### dataSourceViewDataKey `System.String`
The data source view data key.

### Splitter
Creates a Splitter

#### Example
    <%= Html.Kendo().Splitter()
        .Name("Splitter");
        %>

### TabStrip
Creates a new TabStrip.

#### Example
    <%= Html.Kendo().TabStrip()
        .Name("TabStrip")
        .Items(items =>
        {
        items.Add().Text("First");
        items.Add().Text("Second");
        })
        %>

### DateTimePicker
Creates a new DateTimePicker.

#### Example
    <%= Html.Kendo().DateTimePicker()
        .Name("DateTimePicker")
        %>

### DatePicker
Creates a new DatePicker.

#### Example
    <%= Html.Kendo().DatePicker()
        .Name("DatePicker")
        %>

### TimePicker
Creates a new TimePicker.

#### Example
    <%= Html.Kendo().TimePicker()
        .Name("TimePicker")
        %>

### Calendar
Creates a new Calendar.

#### Example
    <%= Html.Kendo().Calendar()
        .Name("Calendar")
        %>

### PanelBar
Creates a new PanelBar.

#### Example
    <%= Html.Kendo().PanelBar()
        .Name("PanelBar")
        .Items(items =>
        {
        items.Add().Text("First");
        items.Add().Text("Second");
        })
        %>

### TreeView
Creates a TreeView

#### Example
    <%= Html.Kendo().TreeView()
        .Name("TreeView")
        .Items(items => { /* add items here */ });
        %>

### NumericTextBox
Creates a new !:NumericTextBox{double}.

#### Example
    <%= Html.Kendo().NumericTextBox()
        .Name("NumericTextBox")
        %>

#### Returns
Returns !:NumericTextBoxBuilder{double}.

### CurrencyTextBox
Creates a new CurrencyTextBox.

#### Example
    <%= Html.Kendo().CurrencyTextBox()
        .Name("CurrencyTextBox")
        %>

#### Returns
Returns !:NumericTextBoxBuilder{decimal}.

### PercentTextBox
Creates a new PercentTextBox.

#### Example
    <%= Html.Kendo().PercentTextBox()
        .Name("PercentTextBox")
        %>

#### Returns
Returns !:NumericTextBoxBuilder{double}.

### IntegerTextBox
Creates a new IntegerTextBox.

#### Example
    <%= Html.Kendo().IntegerTextBox()
        .Name("IntegerTextBox")
        %>

#### Returns
Returns !:NumericTextBoxBuilder{int}.

### Window
Creates a new Window.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        %>

### LinearGauge
Creates a new LinearGauge.

#### Example
    <%= Html.Kendo().LinearGauge()
        .Name("linearGauge")
        %>

### RadialGauge
Creates a new RadialGauge.

#### Example
    <%= Html.Kendo().RadialGauge()
        .Name("radialGauge")
        %>

### DropDownList
Creates a new DropDownList.

#### Example
    <%= Html.Kendo().DropDownList()
        .Name("DropDownList")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### ComboBox
Creates a new ComboBox.

#### Example
    <%= Html.Kendo().ComboBox()
        .Name("ComboBox")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### AutoComplete
Creates a new AutoComplete.

#### Example
    <%= Html.Kendo().AutoComplete()
        .Name("AutoComplete")
        .Items(items =>
        {
        items.Add().Text("First Item");
        items.Add().Text("Second Item");
        })
        %>

### Slider`
Creates a new Slider.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        %>

### Slider
Creates a new Slider.

#### Example
    <%= Html.Kendo().Slider()
        .Name("Slider")
        %>

### RangeSlider`
Creates a new RangeSlider.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        %>

### RangeSlider
Creates a new RangeSlider.

#### Example
    <%= Html.Kendo().RangeSlider()
        .Name("RangeSlider")
        %>

### Upload
Creates a Upload

#### Example
    <%= Html.Kendo().Upload()
        .Name("Upload")
        .Async(async => async
        .Save("ProcessAttachments", "Home")
        .Remove("RemoveAttachment", "Home")
        )
        %>

### Chart`
Creates a !:Kendo.Mvc.UI.Chart{T}

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        %>

### Chart`(System.Collections.Generic.IEnumerable{``0})
Creates a new !:Kendo.Mvc.UI.Chart{T} bound to the specified data source.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        %>

#### Parameters

##### data `System.Collections.Generic.IEnumerable{``0}`
The data source.

### Chart`(System.String)
Creates a new !:Kendo.Mvc.UI.Chart{T} bound an item in ViewData.

#### Example
    <%= Html.Kendo().Chart<SalesData>("sales")
        .Name("Chart")
        %>

#### Parameters

##### dataSourceViewDataKey `System.String`
The data source view data key.

### Chart
Creates a new unbound Chart.

#### Example
    <%= Html.Kendo().Chart("sales")
        .Name("Chart")
        .Series(series => {
        series.Bar(new int[] { 1, 2, 3 }).Name("Total Sales");
        })
        %>