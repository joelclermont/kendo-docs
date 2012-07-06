---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### 3.MajorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the major ticks.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MajorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

### 3.MinorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the minor ticks.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MinorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

### 3.MajorGridLines(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the major grid lines.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MajorGridLines(lines => lines.Visible(true))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

### 3.MajorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the major grid lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MajorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The major gridlines width

##### width `System.String`
The major gridlines color (CSS syntax)

### 3.MinorGridLines(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the minor grid lines.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MinorGridLines(lines => lines.Visible(true))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

### 3.MinorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the minor grid lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MinorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The minor gridlines width

##### width `System.String`
The minor gridlines color (CSS syntax)

### 3.Line(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the axis line.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(line => line.Color("#f00"))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

### 3.Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the lines and enables them.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(2, "#f00", ChartDashType.Dot)
        )
        %>

#### Parameters

##### color `System.Int32`
The axis line width

##### width `System.String`
The axis line color (CSS syntax)

### 3.Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder})
Configures the axis labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Labels(labels => labels
        .Color("Red")
        .Visible(true)
        );
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder}`
The configuration action.

### 3.Labels(System.Boolean)
Sets the visibility of numeric axis chart labels.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.Labels(true))
        %>

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

### 3.PlotBands(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0,`1}})
Defines the plot bands items.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands.Add()
        .From(1)
        .To(2)
        )
        %>

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0`
The add action.

### 3.Title(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder})
Configures the chart axis title.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Title(title => title.Text("Axis"))
        )
        %>

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder}`
The configuration action.

### 3.Title(System.String)
Sets the axis title.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Title("Axis")
        )
        %>

#### Parameters

##### title `System.String`
The axis title.

### 3.Color(System.String)
Sets the color for all axis elements. Can be overriden by individual settings.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Color("#ff0000")
        )
        %>

#### Parameters

##### color `System.String`
The axis color.

### 3.Reverse(System.Boolean)
Sets the axis reverse option.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Reverse(true)
        )
        %>

#### Parameters

##### reverse `System.Boolean`
A value indicating if the axis labels should be rendered in reverse.