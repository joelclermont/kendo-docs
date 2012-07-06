---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder})
Configures the client-side events.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder}`
The client events configuration action.

### 1.Theme(System.String)
Sets the theme of the chart.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Theme("Telerik")
        %>

#### Parameters

##### theme `System.String`
The Chart theme.

### 1.ChartArea(System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder})
Sets the Chart area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder}`
The Chart area.

### 1.PlotArea(System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder})
Sets the Plot area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.margin(20))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder}`
The Plot area.

### 1.Title(System.String)
Sets the title of the chart.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Title("Yearly sales")
        %>

#### Parameters

##### title `System.String`
The Chart title.

### 1.Title(System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder})
Defines the title of the chart.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Yearly sales"))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder}`
The configuration action.

### 1.Legend(System.Boolean)
Sets the legend visibility.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Legend(false)
        %>

#### Parameters

##### visible `System.Boolean`
A value indicating whether to show the legend.

### 1.Legend(System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder})
Configures the legend.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(true).Position(ChartLegendPosition.Bottom))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder}`
The configuration action.

### 1.Series(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}})
Defines the chart series.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series =>
        {
        series.Bar(s => s.SalesAmount);
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}}`
The add action.

### 1.SeriesDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}})
Defines the options for all chart series of the specified type.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .SeriesDefaults(series => series.Bar().Stack(true))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}}`
The configurator.

### 1.AxisDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}})
Defines the options for all chart axes of the specified type.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .AxisDefaults(axisDefaults => axisDefaults.MinorTickSize(5))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}}`
The configurator.

### 1.CategoryAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}})
Configures the category axis

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}}`
The configurator

### 1.ValueAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Defines value axis options

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().TickSize(4))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

### 1.XAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Defines X-axis options for scatter charts

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Numeric().Max(4))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

### 1.YAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Configures Y-axis options for scatter charts.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .YAxis(a => a.Numeric().Max(4))
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

### 1.DataSource(System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}})
Data Source configuration

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .DataSource(ds =>
        {
        ds.Ajax().Read(r => r.Action("SalesData", "Chart"));
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}}`
Use the configurator to set different data binding options.

### 1.SeriesColors(System.Collections.Generic.IEnumerable{System.String})
Sets the series colors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .SeriesColors(new string[] { "#f00", "#0f0", "#00f" })
        %>

#### Parameters

##### colors `System.Collections.Generic.IEnumerable{System.String}`
A list of the series colors.

### 1.SeriesColors(System.String[])
Sets the series colors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .SeriesColors("#f00", "#0f0", "#00f")
        %>

#### Parameters

##### colors `System.String[]`
The series colors.

### 1.Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Use it to configure the data point tooltip.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip =>
        {
        tooltip.Visible(true).Format("{0:C}");
        })
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

### 1.Tooltip(System.Boolean)
Sets the data point tooltip visibility.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(true)
        %>

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            

### 1.Transitions(System.Boolean)
Enables or disabled animated transitions on initial load and refresh.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Transitions(false)
        %>

#### Parameters

##### transitions `System.Boolean`

            A value indicating if transition animations should be played.
            