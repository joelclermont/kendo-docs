---
title: TabStrip
slug: tabstrip
publish: true
---

# Server-Side API

## Animations

### Old

    Html.Telerik().TabStrip().Name("SampleTabStrip").Effects(effects => effects.Slide())

### New

    Html.Kendo().TabStrip().Name("SampleTabStrip").Animation(animation => animation.Open(open => open.FadeIn(FadeDirection.Down))

# Client-Side API

## Events

KendoUI Complete for ASP.NET MVC does not support action syntax i.e. “() => {}”

All widgets no longer have the OnLoad event. Please use **$(document).ready()** instead.

### Old

    Html.Telerik().TabStrip().Name("SampleTabStrip").ClientEvents(events => events.OnChange(“change”))

### New

    Html.Kendo().TabStrip().Name("SampleTabStrip").Events(events => events.Change(“change”))