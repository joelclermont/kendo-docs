---
title: Menu
slug: menu
publish: true
---

# Server-side API

## Animations

### Old
    Html.Telerik().Menu().Name("SampleMenu").Effects(effects => effects.Slide())

### New
    Html.Kendo().Menu().Name("SampleMenu").Animation(animation => animation.Open(open => open.FadeIn(FadeDirection.Down))


# Client-side API

## Events

KendoUI Complete for ASP.NET MVC does not support action syntax i.e. “() => {}”

All widgets no longer have the OnLoad event. Please use $(document).ready() instead.

### Old
    Html.Telerik().Menu().Name("Menu").ClientEvents(events => events.OnChange(“change”))

### New
    Html.Kendo().Menu().Name("Menu").Events(events => events.Change(“change”))
