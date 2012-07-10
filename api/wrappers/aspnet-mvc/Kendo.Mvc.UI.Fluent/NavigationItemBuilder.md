---
title:NavigationItemBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.navigationitembuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.NavigationItemBuilder

Defines the fluent interface for configuring navigation items

## Methods

### ToItem
Returns the inner navigation item

### HtmlAttributes(System.Object)
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Attributes(new {@class="first-item"}))
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### HtmlAttributes(System.Collections.Generic.IDictionary<System.String,System.Object>)
Sets the HTML attributes applied to the outer HTML element rendered for the item

#### Parameters

##### attributes `System.Collections.Generic.IDictionary<System.String`
The attributes.

### Text(System.String)
Sets the text displayed by the item.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item"))
        %>

#### Parameters

##### value `System.String`
The value.

### Visible(System.Boolean)
Makes the item visible or not. Invisible items are not rendered in the output HTML.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Visible((bool)ViewData["visible"])
        %>

#### Parameters

##### value `System.Boolean`
The value.

### Enabled(System.Boolean)
Enables or disables the item. Disabled item cannot be clicked, expanded or open (depending on the item type - menu, tabstrip, panelbar).

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Enabled((bool)ViewData["enabled"])
        %>

### Selected(System.Boolean)
Selects or unselects the item. By default items are not selected.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Selected(true))
        %>

### Route(System.String,System.Web.Routing.RouteValueDictionary)
Sets the route to which the item should navigate.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Route("Default", new RouteValueDictionary{{"id", 1}}))
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Route(System.String,System.Object)
Sets the route to which the item should navigate.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Route("Default", new {id, 1}))
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

##### routeValues `System.Object`
The route values.

### Route(System.String)
Sets the route to which the item should navigate.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").Route("Default"))
        %>

#### Parameters

##### routeName `System.String`
Name of the route.

### Action(System.Web.Routing.RouteValueDictionary)
Sets the action to which the item should navigate

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("Index").Action(MVC.Home.Index(3).GetRouteValueDictionary()))
        %>

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

### Action(System.String,System.String,System.Web.Routing.RouteValueDictionary)
Sets the action to which the item should navigate

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("Index").Action("Index", "Home", new RouteValueDictionary{{"id", 1}}))
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values.

### Action(System.String,System.String,System.Object)
Sets the action to which the item should navigate

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("Index").Action("Index", "Home", new {id, 1}))
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

##### routeValues `System.Object`
The route values.

### Action(System.String,System.String)
Sets the action to which the item should navigate

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("Index").Action("Index", "Home"))
        %>

#### Parameters

##### actionName `System.String`
Name of the action.

##### controllerName `System.String`
Name of the controller.

### Url(System.String)
Sets the URL to which the item should navigate

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("www.example.com").Url("http://www.example.com"))
        %>

#### Parameters

##### value `System.String`
The value.

### ImageUrl(System.String)
Sets the URL of the image that should be displayed by the item.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("First Item").ImageUrl("~/Content/first.png"))
        %>

#### Parameters

##### value `System.String`
The value.

### ImageHtmlAttributes(System.Object)
Sets the HTML attributes for the item image.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items
        .Add().Text("First Item")
        .ImageUrl("~/Content/first.png")
        .ImageHtmlAttributes(new {@class="first-item-image"}))
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### ImageHtmlAttributes(System.Collections.Generic.IDictionary<System.String,System.Object>)
Sets the HTML attributes for the item image.

#### Parameters

##### attributes `System.Collections.Generic.IDictionary<System.String`
The attributes.

### SpriteCssClasses(System.String[])
Sets the sprite CSS class names.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items
        .Add().Text("First Item")
        .SpriteCssClasses("icon", "first-item")
        %>

#### Parameters

##### cssClasses `System.String[]`
The CSS classes.

### Content(System.Action)
Sets the HTML content which the item should display.

#### Parameters

##### value `System.Action`
The action which renders the content.

### Content(System.Func<System.Object,System.Object>)
Sets the HTML content which the item should display.

#### Parameters

##### value `System.Func<System.Object`
The content wrapped in a regular HTML tag or text tag (Razor syntax).

### Content(System.String)
Sets the HTML content which the item should display as a string.

#### Parameters

##### value `System.String`
The action which renders the content.

### ContentHtmlAttributes(System.Object)
Sets the HTML attributes of the content element of the item.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items
        .Add().Text("First Item")
        .Content(() => { %> <strong>First Item Content</strong> <% })
        .ContentHtmlAttributes(new {@class="first-item-content"})
        %>

#### Parameters

##### attributes `System.Object`
The attributes.

### ContentHtmlAttributes(System.Collections.Generic.IDictionary<System.String,System.Object>)
Sets the HTML attributes of the content element of the item.

#### Parameters

##### attributes `System.Collections.Generic.IDictionary<System.String`
The attributes.

### Action<T1>(System.Linq.Expressions.Expression<System.Action<T1>>)
Makes the item navigate to the specified controllerAction method.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items
        .Add().Text("First Item")
        .Action<HomeController>(controller => controller.Index()))
        %>

#### Parameters

##### controllerAction `System.Linq.Expressions.Expression<System.Action<T1>>`
The action.

### Encoded(System.Boolean)
Sets whether the Text property should be encoded when the item is rendered.

#### Example
    <%= Html.Kendo().Menu()
        .Name("Menu")
        .Items(items => items.Add().Text("<strong>First Item</strong>").Encoded(false))
        %>

#### Parameters

##### isEncoded `System.Boolean`
Whether the property should be encoded. Default: true.