---
title: Ajax Binding
publish: true
---

### Ajax Binding

When configured for ajax binding the Kendo Chart for ASP.NET MVC will make an ajax requests to populate its series.

To configure the Kendo Chart for ajax binding follow these steps:

1.  Add a new action method which will return data to populate the chart:

    public ActionResult InternetUsers_Read()
    {
    var data = ChartDataRepository.InternetUsers();
    }
            2.  Return the data&nbsp;as JSON:

    public ActionResult InternetUsers_Read()
    {
    var data = ChartDataRepository.InternetUsers();
    
    return Json(data);
    }
        3.  In the view configure the chart to use the action method created in the previous steps:

#### WebForms
 
    <%: Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
        .Name("internetUsersChart")
        .DataSource(dataSource => dataSource
            .Read(read => read.Action("InternetUsers_Read", "Home")) // Specify the action method and controller name
        )
    &nbsp; &nbsp; &nbsp; &nbsp; .Series(series => {
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; series.Bar(d => d.Value)
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Name("United States");
    &nbsp; &nbsp; &nbsp; &nbsp; })
    &nbsp; &nbsp; &nbsp; &nbsp; .CategoryAxis(axis => axis
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Categories(model => model.Year)
    &nbsp; &nbsp; &nbsp; &nbsp; )
    %>
              
#### Razor
 
    @(Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
    &nbsp; &nbsp; &nbsp; &nbsp; .Name("internetUsersChart")
    &nbsp; &nbsp; &nbsp; &nbsp; .DataSource(dataSource => dataSource
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Read(read => read.Action("InternetUsers_Read", "Home")) // Specify the action method and controller name
    &nbsp; &nbsp; &nbsp; &nbsp; )
    &nbsp; &nbsp; &nbsp; &nbsp; .Series(series => {
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; series.Bar(d => d.Value)
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Name("United States");
    &nbsp; &nbsp; &nbsp; &nbsp; })
    &nbsp; &nbsp; &nbsp; &nbsp; .CategoryAxis(axis => axis
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Categories(model => model.Year)
    &nbsp; &nbsp; &nbsp; &nbsp; )
    )  

### Pass Additional Data to Action Method

To pass additional parameters to the action method use the `Data` setting. Provide the name of a JavaScript function which will return an object
containing the additional data:

  

#### Action method
 
    public ActionResult InternetUsers_Read(string country)
    {
    //Implementation omitted
    }
      

#### WebForms - Send additional data
 
    <%: Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
    &nbsp; &nbsp; &nbsp; &nbsp; .Name("internetUsersChart")
    &nbsp; &nbsp; &nbsp; &nbsp; .DataSource(dataSource => dataSource
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Read(read => read.Action("InternetUsers_Read", "Home"))
            .Data("additionalData")
        )
    &nbsp; &nbsp; &nbsp; &nbsp; .Series(series => {
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; series.Bar(d => d.Value)
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Name("United States");
    &nbsp; &nbsp; &nbsp; &nbsp; })
    &nbsp; &nbsp; &nbsp; &nbsp; .CategoryAxis(axis => axis
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Categories(model => model.Year)
    &nbsp; &nbsp; &nbsp; &nbsp; )
    %>
    <script>
    function additionalData() {
        return {
            country: "United States"
        };
    }
    </script>
      

#### Razor - Send additional data
 
    @(Html.Kendo().Chart<MvcApplication1.Models.InternetUsers>()
    &nbsp; &nbsp; &nbsp; &nbsp; .Name("internetUsersChart")
    &nbsp; &nbsp; &nbsp; &nbsp; .DataSource(dataSource => dataSource
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Read(read => read.Action("InternetUsers_Read", "Home"))
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Data("additionalData")
    &nbsp; &nbsp; &nbsp; &nbsp; )
    &nbsp; &nbsp; &nbsp; &nbsp; .Series(series => {
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; series.Bar(d => d.Value)
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Name("United States");
    &nbsp; &nbsp; &nbsp; &nbsp; })
    &nbsp; &nbsp; &nbsp; &nbsp; .CategoryAxis(axis => axis
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; .Categories(model => model.Year)
    &nbsp; &nbsp; &nbsp; &nbsp; )
    )
    <script>
    function additionalData() {
        return {
            country: "United States"
        };
    }
    </script>
     