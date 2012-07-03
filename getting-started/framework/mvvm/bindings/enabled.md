---
title: Enabled
publish: true
---

### Enabled binding

The `enabled` binding enables the target DOM element (or widget) if the View-Model value is `true`.
If the View-Model value is `false` the target DOM element (or widget) will be disabled.

The `enabled` binding supports only input HTML elements: `input`, `select` and `textarea`.
When an input element is disabled the end user cannot change its value (type in text or choose a different option).

  

#### Using the enable binding
 
    <div id="view">
    <input type="text" data-bind="value: name, enabled: isNameEnabled" />
    <button data-bind="click: enableInput">Enable</button>
    
    <script>
    var viewModel = kendo.obsevable({
        isNameEnabled: false,
        name: "John Doe",
        enableInput: function() {
            this.set("isNameEnabled", true);
        }
    });
    
    kendo.bind($("#view"), viewModel);
    </script>
     </div> 

In this example the input element will be initially disabled because the value of the `isNameEnabled` field
is `false`. When the user presses the button the input will be enabled because the value of the `isNameEnabled`
field is set to `true`.

### Non-boolean values

Non-boolean values such as `0`, `null`, `undefined` and `""` are treated as `false`
by the <span style="font-family: monospace;">enabled&nbsp;</span>binding. All other values are treated as `true`.