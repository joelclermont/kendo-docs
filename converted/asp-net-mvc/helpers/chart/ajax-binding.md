---
title: Ajax Binding
publish: true
---

## Ajax Binding

When configured for ajax binding the Kendo Chart for ASP.NET MVC will make an ajax requests to populate its series.

To configure the Kendo Chart for ajax binding follow these steps:

1.  Add a new action method which will return data to populate the chart:

    public ActionResult InternetUsers_Read()
    {
        var data = ChartDataRepository.InternetUsers();
    }
2.  Return the data as JSON:

    public ActionResult InternetUsers_Read()
    {
        var data = ChartDataRepository.InternetUsers();

        return Json(data);
    }
3.  In the view configure the chart to use the action method created in the previous steps:
- WebForms

        <%: Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
            .Name("internetUsersChart")
            .DataSource(dataSource => dataSource
                .Read(read => read.Action("InternetUsers_Read", "Home")) // Specify the action method and controller name
            )
                .Series(series => {
                    series.Bar(d => d.Value)
                        .Name("United States");
                })
                .CategoryAxis(axis => axis
                    .Categories(model => model.Year)
                )
        %>
- Razor

        @(Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
                .Name("internetUsersChart")
                .DataSource(dataSource => dataSource
                    .Read(read => read.Action("InternetUsers_Read", "Home")) // Specify the action method and controller name
                )
                .Series(series => {
                    series.Bar(d => d.Value)
                        .Name("United States");
                })
                .CategoryAxis(axis => axis
                    .Categories(model => model.Year)
                )
        )

## Pass Additional Data to Action Method

To pass additional parameters to the action method use the `Data` setting. Provide the name of a JavaScript function which will return an object
containing the additional data:

### Action method

    public ActionResult InternetUsers_Read(string country)
    {
        //Implementation omitted
    }


### WebForms - Send additional data

    <%: Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
            .Name("internetUsersChart")
            .DataSource(dataSource => dataSource
                .Read(read => read.Action("InternetUsers_Read", "Home"))
            .Data("additionalData")
        )
            .Series(series => {
                series.Bar(d => d.Value)
                    .Name("United States");
            })
            .CategoryAxis(axis => axis
                .Categories(model => model.Year)
            )
    %>
    <script>
    function additionalData() {
        return {
            country: "United States"
        };
    }
    </script>


### Razor - Send additional data

    @(Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
            .Name("internetUsersChart")
            .DataSource(dataSource => dataSource
                .Read(read => read.Action("InternetUsers_Read", "Home"))
                .Data("additionalData")
            )
            .Series(series => {
                series.Bar(d => d.Value)
                    .Name("United States");
            })
            .CategoryAxis(axis => axis
                .Categories(model => model.Year)
            )
    )
    <script>
    function additionalData() {
        return {
            country: "United States"
        };
    }
    </script>

