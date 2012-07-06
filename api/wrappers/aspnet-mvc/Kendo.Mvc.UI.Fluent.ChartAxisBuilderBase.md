---
title:Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxisbuilderbase
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisBuilderBase

## Methods

### 3.MajorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the major ticks.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MajorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

### 3.MinorTicks(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder})
Configures the minor ticks.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTicksBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart(Model)
        .Name("Chart")
        .ValueAxis(axis => axis
        .MinorTicks(ticks => ticks
        .Visible(false)
        )
        )
        %>

### 3.MajorGridLines(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the major grid lines.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MajorGridLines(lines => lines.Visible(true))
        )
        %>

### 3.MajorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the major grid lines and enables them.

#### Parameters

##### color `System.Int32`
The major gridlines width

##### width `System.String`
The major gridlines color (CSS syntax)

#### Parameters

##### color `System.Int32`
The major gridlines width

##### width `System.String`
The major gridlines color (CSS syntax)

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MajorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

### 3.MinorGridLines(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the minor grid lines.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MinorGridLines(lines => lines.Visible(true))
        )
        %>

### 3.MinorGridLines(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the minor grid lines and enables them.

#### Parameters

##### color `System.Int32`
The minor gridlines width

##### width `System.String`
The minor gridlines color (CSS syntax)

#### Parameters

##### color `System.Int32`
The minor gridlines width

##### width `System.String`
The minor gridlines color (CSS syntax)

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .MinorGridLines(2, "red", ChartDashType.Dot)
        )
        %>

### 3.Line(System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder})
Configures the axis line.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartLineBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(line => line.Color("#f00"))
        )
        %>

### 3.Line(System.Int32,System.String,Kendo.Mvc.UI.ChartDashType)
Sets color and width of the lines and enables them.

#### Parameters

##### color `System.Int32`
The axis line width

##### width `System.String`
The axis line color (CSS syntax)

#### Parameters

##### color `System.Int32`
The axis line width

##### width `System.String`
The axis line color (CSS syntax)

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Line(2, "#f00", ChartDashType.Dot)
        )
        %>

### 3.Labels(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder})
Configures the axis labels.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisLabelsBuilder}`
The configuration action.

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

### 3.Labels(System.Boolean)
Sets the visibility of numeric axis chart labels.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

#### Parameters

##### visible `System.Boolean`
The visibility. The default value is false.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis.Labels(true))
        %>

### 3.PlotBands(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0,`1}})
Defines the plot bands items.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0`
The add action.

#### Parameters

##### addAction `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisPlotBandsFactory{`0`
The add action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .PlotBands.Add()
        .From(1)
        .To(2)
        )
        %>

### 3.Title(System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder})
Configures the chart axis title.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder}`
The configuration action.

#### Parameters

##### configurator `System.Action{Kendo.Mvc.UI.Fluent.ChartAxisTitleBuilder}`
The configuration action.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Title(title => title.Text("Axis"))
        )
        %>

### 3.Title(System.String)
Sets the axis title.

#### Parameters

##### title `System.String`
The axis title.

#### Parameters

##### title `System.String`
The axis title.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Title("Axis")
        )
        %>

### 3.Color(System.String)
Sets the color for all axis elements. Can be overriden by individual settings.

#### Parameters

##### color `System.String`
The axis color.

#### Parameters

##### color `System.String`
The axis color.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Color("#ff0000")
        )
        %>

### 3.Reverse(System.Boolean)
Sets the axis reverse option.

#### Parameters

##### reverse `System.Boolean`
A value indicating if the axis labels should be rendered in reverse.

#### Parameters

##### reverse `System.Boolean`
A value indicating if the axis labels should be rendered in reverse.

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Categories(s => s.DateString)
        .Reverse(true)
        )
        %>