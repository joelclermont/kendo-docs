---
title: ComboBox
slug: combobox
publish: true
---

# Server-Side API

## DataBinding

Binding to **List<SelectListItem>** collection
 
### Old
 
    Html.Telerik().ComboBox()
        .Name(“Combo”)
        .BindTo(new SelectList(Model.Products, "ProductID", "ProductName"))
 
### New
 
    Html.Kendo().ComboBox()
        .Name(“Combo”)
        .BindTo(new SelectList(Model.Products, "ProductID", "ProductName"))
        .DataTextField(“Text”)
        .DataValueField(“Value”)
 
Manually create items:
 
### Old
 
    Html.Telerik().ComboBox()
    .Name(“Combo”)
    . Items( items => items.Add().Text("Item1").Value("1"))
 
### New
 
    Html.Kendo().ComboBox()
        .Name(“Combo”)
        .Items( items => items.Add().Text("Item1").Value("1"))
        .DataTextField(“Text”)
        .DataValueField(“Value”)
 
Ajax binding:
 
### Old

    Html.Telerik().ComboBox()
        .Name(“Combo”)
        .DataBinding(binding => binding.Ajax().Select(“_Select”, “Combo”))
 
### New
 
    Html.Kendo().ComboBox().Name(“Combo”)
        .DataSource(source => {
            source.Read(read =>
            {
                read.Action("GetProducts", "Home");
            })
            .ServerFiltering(true);
        })
        .DataTextField(“Text”)
        .DataValueField(“Value”)
 
Define **Delay**:
 
### Old
 
    Html.Telerik().ComboBox()
        .Name(“Combo”)
        .DataBinding(binding => binding.Ajax().Delay(300))
 
### New
 
    Html.Kendo().ComboBox()
        .Name(“Combo”)
        .Delay(300)
     
Define **ServerFiltering**:
 
### Old

Not supported
 
### New
 
    Html.Kendo().ComboBox().Name(“Combo”)
        .DataSource(source => {
            source.Read(read =>
            {
                read.Action("GetProducts", "Home");
            }).ServerFiltering(true);
        })
        .DataTextField(“Text”)
        .DataValueField(“Value”)
     
Send parameters to the server:
 
### Old
    <%= Html.Telerik().ComboBox()
        .Name("AjaxComboBox")
        …
        .ClientEvents(events => events.OnDataBinding("onComboBoxDataBinding"))
    %>

    <script type="text/javascript">       
        function onComboBoxDataBinding(e) {
            e.data = $.extend({}, e.data, { filterMode: $('#ComboBoxAttributes_FilterMode').data('tDropDownList').value() });
        }
    </script>
 
### New
 
    Html.Kendo().ComboBox().Name(“Combo”)
        .DataSource(source => {
            source.Read(read =>
            {
                read.Action("GetProducts", "Home")
                    .Data(“addData”);
            })     
        })
        .DataTextField(“Text”)
        .DataValueField(“Value”)
  
    <script type="text/javascript">
        function addData() {
            return { text : “Chai” }
        }
    </script>
    
Bind to a collection which is not a **List<SelectListItem>**:
 
### Old

Not supported
 
### New
 
    Html.Kendo().ComboBox().Name(“Combo”)
        .DataTextField(“CompanyName”)
        .DataValueField(“CompanyID”)
        .BindTo(List<Company>);
    })
    
## Other Options

### Filter
 
### Old

    <%= Html.Telerik().ComboBox()
        .Name("AjaxComboBox")
        .Filterable(filtering =>
        {
            filtering.FilterMode(AutoCompleteFilterMode.Contains);                             
        })
 
### New

    @(Html.Kendo().ComboBox()
        .Name("fabric")
        .Filter(FilterType.StartsWith)
    )
 
### Minimum Characters
 
### Old

    <%= Html.Telerik().ComboBox()
        .Name("AjaxComboBox")
        .Filterable(filtering =>
        {
            filtering.MinimumChars(2);
        })
 
### New
 
    @(Html.Kendo().ComboBox()
        .Name("fabric")
        .MinLength (2)
    )
    
Define suggestion (autofill) of the ComboBox:
 
### Old
 
    Html.Telerik().ComboBox().Name("AjaxComboBox").AutoFill(true)
 
### New

    Html.Kendo().ComboBox().Name("AjaxComboBox").Suggest(true)

Set placeholder:
 
### Old

    //Create item with text  “Select…” and value “”
    Html.Telerik().ComboBox().Name("AjaxComboBox").Placeholder(“Select…”)
 
### New

    //Html5 placeholder
    Html.Kendo().ComboBox().Name("AjaxComboBox"). Placeholder (“2”)

Define animations:
 
### Old

    Html.Telerik().ComboBox().Name("AjaxComboBox").Effects(effects => effects.Slide())
 
### New
    Html.Kendo().ComboBox().Name("AjaxComboBox") .Animation(animation => animation.Open(open => open.FadeIn(FadeDirection.Down))

Set **AutoBind**:

### Old

Not supported (when Ajax binding always autoBind: false)

### New

Html.Kendo().ComboBox().Name("Combo").AutoBind(false)

Set **SelectedText** when **AutoBind** false:

### Old
    
    Html.Telerik().ComboBox().Name("Combo")
        .DataBinding(binding => binding.Ajax().Select(“”, “”))
        .InputHtmlAttribute(new { value = “Chai” })

### New
Html.Kendo().ComboBox().Name("Combo").AutoBind(false).Text(“Chai”)

Highlight first item:

### Old
    
    HighlightFirstMatch(true)
 
### New
    
    HighlightFirst (true)

Kendo does not support action syntax - “() => {}”.  All widgets does not have **OnLoad** event.
 
### Old

    Html.Telerik().ComboBox().Name("Combo").ClientEvents( events => events.OnChange(“change”))
 
### New

    Html.Kendo().ComboBox().Name("Combo").Events( events => events.Change(“change”))

Define Template:

### Old

Not supported
 
### New
    
    Html.Kendo().ComboBox().Name("Combo").Template(“#= data.CompanyName #”)

Define Height of popup element:

### Old

    Html.Telerik().ComboBox().Name("Combo").DropDownHtmlAttributes( new style { height = “300px” })
 
### New
    
    Html.Kendo().ComboBox().Name("Combo").Height(300)

Cascading functionality:
 
### Old

    Html.Telerik().ComboBox().Name("Combo").CascadeTo(“Id of the child ComboBox”)
 
### New
    
    Html.Kendo().ComboBox().Name("Combo").CascadeFrom(“Id of the parent ComboBox”)

Encode:
 
### Old

    Encode(false)
 
### New
    Template(“ #= data.Text #”)

## Client-Side API

### MVC -> Kendo
 
##### value

value

##### open

open

##### close

close

##### highlight

None

##### text

text
##### select

select

##### enable

enable

##### disable

enable(false)

##### dataBind

dataSource.data(data)

##### reload

dataSource.read()
