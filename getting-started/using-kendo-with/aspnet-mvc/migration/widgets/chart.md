---
title: Chart
slug: chart
publish: true
---

# Server-side API

## DataBinding

DataBinding configuration is moved to DataSource:

### Old
    Html.Telerik().Chart<SalesData>()
    .Name("Chart")
    .DataBinding(dataBinding => dataBinding.Ajax().Select("_AjaxBinding", "Chart"))

### New
    Html.Kendo().Chart<SalesData>()
    .Name("Chart")
    .DataSource(ds => ds.Read(read => read.Action("_AjaxBinding", "Chart")))

# Client-side API

## Events

KendoUI Complete for ASP.NET MVC does not support action syntax i.e. “() => {}”

All widgets no longer have the OnLoad event. Please use $(document).ready() instead.

### Old
    .ClientEvents(events => events.OnError("onError"))

### New
    .DataSource(ds => ds.Events(events => events.Error("error")))
