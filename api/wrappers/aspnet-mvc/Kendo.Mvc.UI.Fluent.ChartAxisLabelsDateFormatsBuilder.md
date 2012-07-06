---
title:Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.chartaxislabelsdateformatsbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.ChartAxisLabelsDateFormatsBuilder

## Methods

### Hours(System.String)
Sets the date format when the base date unit is

#### Parameters

##### format `System.String`
The date format.

#### Parameters

##### format `System.String`
The date format.

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

### Days(System.String)
Sets the date format when the base date unit is

#### Parameters

##### format `System.String`
The date format.

#### Parameters

##### format `System.String`
The date format.

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

### Months(System.String)
Sets the date format when the base date unit is

#### Parameters

##### format `System.String`
The date format.

#### Parameters

##### format `System.String`
The date format.

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

### Years(System.String)
Sets the date format when the base date unit is

#### Parameters

##### format `System.String`
The date format.

#### Parameters

##### format `System.String`
The date format.

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