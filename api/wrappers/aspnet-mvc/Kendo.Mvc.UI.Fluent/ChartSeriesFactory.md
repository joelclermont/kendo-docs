---
title:Kendo.Mvc.UI.Fluent.ChartSeriesFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesFactory

Creates series for the .

## Methods

### Bar``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,System.String}})
Defines bound bar series.

#### Parameters

##### valueExpression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the point value from the chart model

##### colorExpression ```0}}`
The expression used to extract the point color from the chart model

### Bar(System.String,System.String)
Defines bound bar series.

#### Parameters

##### valueMemberName `System.String`
The name of the value member.

##### colorMemberName `System.String`
The name of the color member.

### Bar(System.Type,System.String,System.String)
Defines bound bar series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### valueMemberName `System.String`
The name of the value member.

##### colorMemberName `System.String`
The name of the color member.

### Bar(System.Collections.IEnumerable)
Defines bar series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to.

### Column``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,System.String}})
Defines bound column series.

#### Parameters

##### valueExpression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the point value from the chart model

##### colorExpression ```0}}`
The expression used to extract the point color from the chart model

### Column(System.String,System.String)
Defines bound bar series.

#### Parameters

##### valueMemberName `System.String`
The name of the value member.

##### colorMemberName `System.String`
The name of the color member.

### Column(System.Type,System.String,System.String)
Defines bound bar series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### valueMemberName `System.String`
The name of the value member.

##### colorMemberName `System.String`
The name of the color member.

### Column(System.Collections.IEnumerable)
Defines bar series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Line``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines bound line series.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the series value from the chart model

### Line(System.String)
Defines bound line series.

#### Parameters

##### memberName `System.String`
The name of the value member.

### Line(System.Type,System.String)
Defines bound line series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### memberName `System.String`
The name of the value member.

### Line(System.Collections.IEnumerable)
Defines line series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### VerticalLine``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines bound vertical line series.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the series value from the chart model

### VerticalLine(System.String)
Defines bound vertical line series.

#### Parameters

##### memberName `System.String`
The name of the value member.

### VerticalLine(System.Type,System.String)
Defines bound vertical line series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### memberName `System.String`
The name of the value member.

### VerticalLine(System.Collections.IEnumerable)
Defines vertical line series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Area``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines bound area series.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the series value from the chart model.

### Area(System.String)
Defines bound area series.

#### Parameters

##### memberName `System.String`
The name of the value member.

### Area(System.Type,System.String)
Defines bound area series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### memberName `System.String`
The name of the value member.

### Area(System.Collections.IEnumerable)
Defines area series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### VerticalArea``1(System.Linq.Expressions.Expression{System.Func{`0,``0}})
Defines bound vertical area series.

#### Parameters

##### expression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the series value from the chart model.

### VerticalArea(System.String)
Defines bound vertical area series.

#### Parameters

##### memberName `System.String`
The name of the value member.

### VerticalArea(System.Type,System.String)
Defines bound vertical area series.

#### Parameters

##### memberType `System.Type`
The type of the value member.

##### memberName `System.String`
The name of the value member.

### VerticalArea(System.Collections.IEnumerable)
Defines vertical area series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Scatter``2(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,``1}})
Defines bound scatter series.

#### Parameters

##### xValueExpression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the X value from the chart model

##### yValueExpression ```0}}`
The expression used to extract the Y value from the chart model

### Scatter(System.String,System.String)
Defines bound scatter series.

#### Parameters

##### xMemberName `System.String`
The name of the X value member.

##### yMemberName `System.String`
The name of the Y value member.

### Scatter(System.Collections.IEnumerable)
Defines scatter series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### ScatterLine``2(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,``1}})
Defines bound scatter line series.

#### Parameters

##### xValueExpression `System.Linq.Expressions.Expression{System.Func{`0`
The expression used to extract the X value from the chart model

##### yValueExpression ```0}}`
The expression used to extract the Y value from the chart model

### ScatterLine(System.String,System.String)
Defines bound scatter line series.

#### Parameters

##### xMemberName `System.String`
The name of the X value member.

##### yMemberName `System.String`
The name of the Y value member.

### ScatterLine(System.Collections.IEnumerable)
Defines scatter line series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Bubble``3(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,``1}},System.Linq.Expressions.Expression{System.Func{`0,``2}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.Boolean}})
Defines bound bubble series.

### Bubble(System.String,System.String,System.String,System.String,System.String,System.String)
Defines bound bubble series.

### Bubble(System.Type,System.String,System.String,System.String,System.String,System.String,System.String)
Defines bound bubble series.

### Bubble(System.Collections.IEnumerable)
Defines bubble series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Pie``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.Boolean}},System.Linq.Expressions.Expression{System.Func{`0,System.Boolean}})
Defines bound pie series.

### Pie(System.String,System.String,System.String,System.String,System.String)
Defines bound pie series.

### Pie(System.Type,System.String,System.String,System.String,System.String,System.String)
Defines bound pie series.

### Pie(System.Collections.IEnumerable)
Defines pie series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to

### Donut``1(System.Linq.Expressions.Expression{System.Func{`0,``0}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.String}},System.Linq.Expressions.Expression{System.Func{`0,System.Boolean}},System.Linq.Expressions.Expression{System.Func{`0,System.Boolean}})
Defines bound pie series.

### Donut(System.String,System.String,System.String,System.String,System.String)
Defines bound donut series.

### Donut(System.Type,System.String,System.String,System.String,System.String,System.String)
Defines bound donut series.

### Donut(System.Collections.IEnumerable)
Defines donut series bound to inline data.

#### Parameters

##### data `System.Collections.IEnumerable`
The data to bind to