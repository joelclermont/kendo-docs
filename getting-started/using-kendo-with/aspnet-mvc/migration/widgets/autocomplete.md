---
title: AutoComplete
slug: autocomplete
publish: true
---

# Server-Side API

All changes described in the [ComboBox](combobox) are applicable to the AutoComplete. AutoComplete can be bound to any collection, just define the DataTextField.

## Other Options

**Separator**:

### Old

	Html.Telerik().AutoComplete().Name(“AutoComplete”).Multiple(m => m.Separator(“, “))
 
### New

	Html.Kendo ().AutoComplete().Name(“AutoComplete”).Separator(“, “)