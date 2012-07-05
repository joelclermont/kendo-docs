---
title: Disabled
slug: mvv-disabled-binding
publish: true
---

# Disabled binding

The `disabled` binding disables the target DOM element (or widget) if the View-Model value is `true`.
If the View-Model value is `false` the target DOM element (or widget) will be enabled.

The `disabled` binding supports only input HTML elements: `input`, `select` and `textarea`.
When an input element is disabled the end user cannot change its value (type in text or choose a different option).

## Using the disabled binding

    <div id="view">
    <input type="text" data-bind="value: name, disabled: isNameDisabled" />
    <button data-bind="click: disableInput">Disable</button>

    <script>
    var viewModel = kendo.observable({
        isNameDisabled: false,
        name: "John Doe",
        disableInput: function() {
            this.set("isNameDisabled", false);
        }
    });

    kendo.bind($("#view"), viewModel);
    </script>
     </div>

In this example the input element will be initially enabled because the value of the `isNameDisabled` field
is `false`. When the user presses the button the input will be disabled because the value of the `isNameDisabled`
field is set to `false`.

## Non-boolean values

Non-boolean values such as `0`, `null`, `undefined` and `""` are treated as `false`
by the `disabled` binding. All other values are treated as `true`.
