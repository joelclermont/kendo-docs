---
title:Kendo.Mvc.UI.Fluent.ChartBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartBuilder

## Methods

### 1.Events(System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder})
Configures the client-side events.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder}`
The client events configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartEventBuilder}`
The client events configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Events(events => events
        .OnLoad("onLoad")
        )
        %>

### 1.Theme(System.String)
Sets the theme of the chart.

#### Parameters

##### theme `System.String`
The Chart theme.

#### Parameters

##### theme `System.String`
The Chart theme.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Theme("Telerik")
        %>

### 1.ChartArea(System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder})
Sets the Chart area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder}`
The Chart area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAreaBuilder}`
The Chart area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .ChartArea(chartArea => chartArea.margin(20))
        %>

### 1.PlotArea(System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder})
Sets the Plot area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder}`
The Plot area.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.PlotAreaBuilder}`
The Plot area.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .PlotArea(plotArea => plotArea.margin(20))
        %>

### 1.Title(System.String)
Sets the title of the chart.

#### Parameters

##### title `System.String`
The Chart title.

#### Parameters

##### title `System.String`
The Chart title.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Title("Yearly sales")
        %>

### 1.Title(System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder})
Defines the title of the chart.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTitleBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Title(title => title.Text("Yearly sales"))
        %>

### 1.Legend(System.Boolean)
Sets the legend visibility.

#### Parameters

##### visible `System.Boolean`
A value indicating whether to show the legend.

#### Parameters

##### visible `System.Boolean`
A value indicating whether to show the legend.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Legend(false)
        %>

### 1.Legend(System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder})
Configures the legend.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLegendBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Legend(legend => legend.Visible(true).Position(ChartLegendPosition.Bottom))
        %>

### 1.Series(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}})
Defines the chart series.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}}`
The add action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesFactory{`0}}`
The add action.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .Series(series =>
        {
        series.Bar(s => s.SalesAmount);
        })
        %>

### 1.SeriesDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}})
Defines the options for all chart series of the specified type.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}}`
The configurator.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartSeriesDefaultsBuilder{`0}}`
The configurator.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .SeriesDefaults(series => series.Bar().Stack(true))
        %>

### 1.AxisDefaults(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}})
Defines the options for all chart axes of the specified type.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}}`
The configurator.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisDefaultsBuilder{`0}}`
The configurator.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .AxisDefaults(axisDefaults => axisDefaults.MinorTickSize(5))
        %>

### 1.CategoryAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}})
Configures the category axis

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartCategoryAxisBuilder{`0}}`
The configurator

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        )
        %>

### 1.ValueAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Defines value axis options

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(a => a.Numeric().TickSize(4))
        %>

### 1.XAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Defines X-axis options for scatter charts

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .XAxis(a => a.Numeric().Max(4))
        %>

### 1.YAxis(System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}})
Configures Y-axis options for scatter charts.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartValueAxisFactory{`0}}`
The configurator

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .YAxis(a => a.Numeric().Max(4))
        %>

### 1.DataSource(System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}})
Data Source configuration

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}}`
Use the configurator to set different data binding options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ReadOnlyAjaxDataSourceBuilder{`0}}`
Use the configurator to set different data binding options.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .DataSource(ds =>
        {
        ds.Ajax().Read(r => r.Action("SalesData", "Chart"));
        })
        %>

### 1.SeriesColors(System.Collections.Generic.IEnumerable{System.String})
Sets the series colors.

#### Parameters

##### colors `System.Collections.Generic.IEnumerable{System.String}`
A list of the series colors.

#### Parameters

##### colors `System.Collections.Generic.IEnumerable{System.String}`
A list of the series colors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .SeriesColors(new string[] { "#f00", "#0f0", "#00f" })
        %>

### 1.SeriesColors(System.String[])
Sets the series colors.

#### Parameters

##### colors `System.String[]`
The series colors.

#### Parameters

##### colors `System.String[]`
The series colors.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .SeriesColors("#f00", "#0f0", "#00f")
        %>

### 1.Tooltip(System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder})
Use it to configure the data point tooltip.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartTooltipBuilder}`
Use the configurator to set data tooltip options.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(tooltip =>
        {
        tooltip.Visible(true).Format("{0:C}");
        })
        %>

### 1.Tooltip(System.Boolean)
Sets the data point tooltip visibility.

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            

#### Parameters

##### visible `System.Boolean`

            A value indicating if the data point tooltip should be displayed.
            The tooltip is not visible by default.
            

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Tooltip(true)
        %>

### 1.Transitions(System.Boolean)
Enables or disabled animated transitions on initial load and refresh.

#### Parameters

##### transitions `System.Boolean`

            A value indicating if transition animations should be played.
            

#### Parameters

##### transitions `System.Boolean`

            A value indicating if transition animations should be played.
            

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .Transitions(false)
        %>