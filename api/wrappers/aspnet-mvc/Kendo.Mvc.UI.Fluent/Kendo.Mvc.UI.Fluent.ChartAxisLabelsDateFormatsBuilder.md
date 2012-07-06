---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsdateformatsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder

## Methods

### Hours(System.String)
Sets the date format when the base date unit is

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .DateFormats(formats => formats
        .Hours("HH:mm")
        )
        )
        );
        %>

#### Parameters

##### format `System.String`
The date format.

### Days(System.String)
Sets the date format when the base date unit is

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .DateFormats(formats => formats
        .Days("HH:mm")
        )
        )
        );
        %>

#### Parameters

##### format `System.String`
The date format.

### Months(System.String)
Sets the date format when the base date unit is

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .DateFormats(formats => formats
        .Months("HH:mm")
        )
        )
        );
        %>

#### Parameters

##### format `System.String`
The date format.

### Years(System.String)
Sets the date format when the base date unit is

#### Example
    <%= Html.Kendo().Chart()
        .Name("Chart")
        .CategoryAxis(axis => axis
        .Date()
        .Labels(labels => labels
        .DateFormats(formats => formats
        .Years("HH:mm")
        )
        )
        );
        %>

#### Parameters

##### format `System.String`
The date format.