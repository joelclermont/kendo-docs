---
title:ChartSeriesFactory
slug:aspnetmvc-kendo.mvc.ui.fluent.chartseriesfactory
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartSeriesFactory

Creates series for the !:Chart{TModel}.

## Properties

### Container
The parent Chart

## Methods

### Bar\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>)
Defines bound bar series.

#### Parameters

##### valueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The expression used to extract the point value from the chart model

##### colorExpression `System.Linq.Expressions.Expression<System.Func<T,System.String>>`
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

### Column\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>)
Defines bound column series.

#### Parameters

##### valueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The expression used to extract the point value from the chart model

##### colorExpression `System.Linq.Expressions.Expression<System.Func<T,System.String>>`
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

### Line\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound line series.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### VerticalLine\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound vertical line series.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### Area\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound area series.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### VerticalArea\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound vertical area series.

#### Parameters

##### expression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### Scatter\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound scatter series.

#### Parameters

##### xValueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The expression used to extract the X value from the chart model

##### yValueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### ScatterLine\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>)
Defines bound scatter line series.

#### Parameters

##### xValueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
The expression used to extract the X value from the chart model

##### yValueExpression `System.Linq.Expressions.Expression<System.Func<T,T1>>`
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

### Bubble\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.Boolean\>\>)
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

### Pie\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.Boolean\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.Boolean\>\>)
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

### Donut\<T1\>(System.Linq.Expressions.Expression\<System.Func\<T,T1\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.String\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.Boolean\>\>,System.Linq.Expressions.Expression\<System.Func\<T,System.Boolean\>\>)
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