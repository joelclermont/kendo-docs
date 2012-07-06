---
title:Kendo.Mvc.UI.Fluent.WindowBuilder
slug:aspnetmvc-kendo.mvc.ui.fluent.windowbuilder
publish:true
---

# Kendo.Mvc.UI.Fluent.WindowBuilder

## Methods

### Title(System.String)
Sets title, which appears in the header of the window.

### Content(System.Action)
Sets the HTML content which the window should display.

#### Parameters

##### value `System.Action`
The action which renders the content.

#### Parameters

##### value `System.Action`
The action which renders the content.

#### Example
    <% Html.Kendo().Window()
        .Name("Window")
        .Content(() =>
        {
        %>
        <strong>Window content</strong>
        <%
        })
        %>

### Content(System.Func{System.Object,System.Object})
Sets the HTML content which the window should display

#### Parameters

##### value `System.Func{System.Object`
The Razor inline template

#### Parameters

##### value `System.Func{System.Object`
The Razor inline template

#### Example
    @(Html.Kendo().Window()
        .Name("Window")
        .Content(@<strong> Hello World!</strong>))

### Content(System.String)
Sets the HTML content which the item should display as a string.

#### Parameters

##### value `System.String`
The action which renders the content.

#### Parameters

##### value `System.String`
The action which renders the content.

### LoadContentFrom(System.Web.Routing.RouteValueDictionary)
Sets the Url, which will be requested to return the content.

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

#### Parameters

##### routeValues `System.Web.Routing.RouteValueDictionary`
The route values of the Action method.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .LoadContentFrom(MVC.Home.Index().GetRouteValueDictionary());
        %>

### LoadContentFrom(System.String,System.String)
Sets the Url, which will be requested to return the content.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .LoadContentFrom("AjaxView_OpenSource", "Window")
        %>

### LoadContentFrom(System.String,System.String,System.Object)
Sets the Url, which will be requested to return the content.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

##### routeValues `System.Object`
Route values.

#### Parameters

##### actionName `System.String`
The action name.

##### controllerName `System.String`
The controller name.

##### routeValues `System.Object`
Route values.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .LoadContentFrom("AjaxView_OpenSource", "Window", new { id = 10})
        %>

### LoadContentFrom(System.String)
Sets the Url, which will be requested to return the content.

#### Parameters

##### value `System.String`
The url.

#### Parameters

##### value `System.String`
The url.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .LoadContentFrom(Url.Action("AjaxView_OpenSource", "Window"))
        %>

### Events(System.Action{Kendo.Mvc.UI.Fluent.WindowEventBuilder})
Configures the client-side events.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowEventBuilder}`
The client events action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowEventBuilder}`
The client events action.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Events(events =>
        events.Open("onOpen").Close("onClose")
        )
        %>

### Resizable
Enables windows resizing.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Resizable()
        %>

### Resizable(System.Action{Kendo.Mvc.UI.Fluent.WindowResizingSettingsBuilder})
Configures the resizing ability of the window.

#### Parameters

##### resizingSettingsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowResizingSettingsBuilder}`
Resizing settings action.

#### Parameters

##### resizingSettingsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowResizingSettingsBuilder}`
Resizing settings action.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Resizable(settings =>
        settings.Enabled(true).MaxHeight(500).MaxWidth(500)
        )
        %>

### Actions(System.Action{Kendo.Mvc.UI.Fluent.WindowActionsBuilder})
Configures the window buttons.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowActionsBuilder}`
The buttons configuration action.

#### Parameters

##### clientEventsAction `System.Action{Kendo.Mvc.UI.Fluent.WindowActionsBuilder}`
The buttons configuration action.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Actions(actions =>
        actions.
        )
        %>

### Width(System.Int32)
Sets the width of the window.

### Height(System.Int32)
Sets the height of the window.

### Visible(System.Boolean)
Sets whether the window should be rendered visible.

### Scrollable(System.Boolean)
Sets whether the window should have scrollbars.

### Animation(System.Boolean)
Configures the animation effects of the window.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Parameters

##### enable `System.Boolean`
Whether the component animation is enabled.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Animation(false)

### Animation(System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder})
Configures the animation effects of the panelbar.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder}`
The action that configures the animation.

#### Parameters

##### animationAction `System.Action{Kendo.Mvc.UI.Fluent.PopupAnimationBuilder}`
The action that configures the animation.

#### Example
    <%= Html.Kendo().Window()
        .Name("Window")
        .Animation(animation => animation.Expand)

### Modal(System.Boolean)
Sets whether the window should be modal or not.

### Draggable
Sets whether the window can be moved.

### Draggable(System.Boolean)
Sets whether the window can be moved.