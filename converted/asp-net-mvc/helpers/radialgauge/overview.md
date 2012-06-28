---
title: Overview
publish: true
---

### RadialGauge

The RadialGauge HtmlHelper extension is a server-side wrapper for the [Kendo DataViz RadialGaug](http://www.kendoui.com/documentation/dataviz/radial-gauge/overview.aspx)e widget.

### Getting Started

Here is how to configure a simple Kendo RadialGauge:

1.  Make sure you have followed all the steps from the [Introduction](http://www.kendoui.com/documentation/asp-net-mvc/introduction.aspx) help topic.

2.  Create a new action method which renders the view:

    public ActionResult Index()
    {
    return View();
    }
        3.  Add a RadialGauge:

#### WebForms
 
    <%: Html.Kendo().RadialGauge()
        .Name("radialGauge") // The name of the radialGauge is mandatory. It specifies the "id" attribute of the widget.
        .Scale(scale => scale
            .Min(0) // Set min value of the radialGauge
            .Max(200) // Set min value of the radialGauge
        )
        .Pointer(pointer => pointer
            .Value(10) // Set the value of the radialGauge
        )
    %>
              
#### Razor
 
    <pre class="prettyprint">@(Html.Kendo().RadialGauge()
      .Name("radialGauge") // The name of the radialGauge is mandatory. It specifies the "id" attribute of the widget.
      .Scale(scale => scale
          .Min(0) // Set min value of the radialGauge
          .Max(200) // Set min value of the radialGauge
      )
      .Pointer(pointer => pointer
          .Value(10) // Set the value of the radialGauge
      )
    ) </pre>  

### Accessing an Existing Radial Gauge

You can reference an existing RadialGauge instance via [jQuery.data()](http://api.jquery.com/jQuery.data/).
Once a reference has been established, you can use the [API](http://www.kendoui.com/documentation/dataviz/radial-gauge/methods.aspx) to control its behavior.

  

#### Accessing an existing RadialGauge instance
 
    //Put this after your Kendo RadialGauge for ASP.NET MVC declaration
    <script>
    $(function() {
    // Notice that the Name() of the radialGauge is used to get its client-side instance
    var radialGauge = $("#radialGauge").data("kendoRadialGauge");
    });
    </script>
     