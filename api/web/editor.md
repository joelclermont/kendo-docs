---
title: kendo.ui.Editor
tags: api,web
publish: true
---

# kendo.ui.Editor

## Description



      The Editor allows users to create rich text content by means of a WYSIWYG interfance. The generated widget value is an XHTML markup.
 

### Getting Started

#### Creating an **Editor** from existing HTML element

      <textarea id="editor" rows="10" cols="30"></textarea>

#### Initialize the Kendo Editor

      $(document).ready(function(){
          $("#editor").kendoEditor();
      });

### Configuring the Editor

 If no specific tools are defined, the Editor will create its default set of tools for text formatting.

#### Specifying a set of Editor tools

       $(document).ready(function(){
          $("#editor").kendoEditor({
             tools: [
                 "bold",
                 "italic",
                 "underline",
                 "foreColor"
             ]
          });
      });

### Specifying custom tools


 The Editor functionality can be extended through custom tools, defined in the `tools` array.

#### Adding a custom tool button

       $("#editor").kendoEditor({
           tools: [
               {
                   name: "toolName",
                   tooltip: "Custom editor tool",
                   exec: function(e) {
                       var editor = $(this).data("kendoEditor");
    
                       // execute command
                   }
               }
           ]
       });

The custom buttons get a **k-toolName** CSS class to allow styling. (where `toolName` is the name specified in the custom tool configuration)

## Configuration

### `encoded` : **Boolean** *(default: true)*

 Indicates whether the Editor should submit encoded HTML tags.

#### Example

    $("#editor").kendoEditor({
         encoded: false
     });

### `stylesheets` : **Array** 

Allows custom stylesheets to be included within the editing area.

#### Example

    $("#editor").kendoEditor({
         stylesheets: [
             "common-styles.css",
             "green-theme.css",
         ]
     });

### `tools` : **Array** 

A collection of tools that should render a button, combobox, etc, to interact with the Editor. Custom tools are defined
as a collection of required properties, while the insertHtml  tool requires a collection of text-value pairs

#### Example

    $("#editor").kendoEditor({
         tools: [
         "bold",
         "italic",
         "underline",
         "strikethrough",
         "fontName",
         "fontSize",
         "foreColor",
         "backColor",
         "justifyLeft",
         "justifyCenter",
         "justifyRight",
         "justifyFull",
         "insertUnorderedList",
         "insertOrderedList",
         "indent",
         "outdent",
         "formatBlock",
         "createLink",
         "unlink",
         "insertImage",
         "insertHtml",
         "viewHtml",
         {
             name: "customTool",
             tooltip: "Custom Tool",
             exec: function(e) {
                 var editor = $(this).data("kendoEditor");
                 // ...
             }
         }
         ],
         insertHtml: [
             { text: "label 1", value: "<p>snippet 1</p>" },
             { text: "label 2", value: "<p>snippet 2</p>" }
         ]
     });

## Methods

### createRange

Creates a W3C-compatible **Range** object.

#### Example

    var editor = $("#editor").data("kendoEditor");
    
    var range = editor.createRange();

#### Parameters

##### document `Document`

The document that the range is associated with. If ommited, the document of the editor editing area will be used.

#### Returns

`Range` The created <strong>Range</strong> object.

### encodedValue

Gets the HTML encoded value of the editor.

### exec

Executes an editor command on the currently selected text.

#### Example

    var editor = $("#editor").data("kendoEditor");
    
    editor.exec("bold");
    
    editor.exec("undo");
    
    editor.exec("foreColor", { value: "#ff0000" });

#### Parameters

##### name `String`

The name of the command to be executed.

##### params `String`

The parameters for the executed command.

### focus

Focuses the editable area.

### getRange

Gets a **Range** object form the editable area.

#### Example

    var editor = $("#editor").data("kendoEditor");
    
    var range = editor.getRange();

#### Returns

`Range` A W3C-compatible <strong>Range</strong> object that represents the currently selected text in the editor area.

### getSelection

Gets a W3C-compatible **Selection** object form the editable area.

### paste

Pastes HTML into the editable area.

#### Example

    var editor = $("#editor").data("kendoEditor");
    
    editor.paste("<p>new content</p>");

#### Parameters

##### html `String`

The HTML to be pasted.

### selectedHtml

Serializes the currently selected text to a XHTML string.

#### Returns

`String` The selectied text as valid XHTML.

### selectRange

Focuses the editable area and selects the range described by the range parameter.

#### Example

    var editor = $("#editor").data("kendoEditor"),
        range = editor.createRange();
    
    range.selectNodeContents(editor.body);
    
    editor.selectRange(range);

#### Parameters

##### range `Range`

The **Range** object that describes the new selection.

### update

Serializes the current state of the editable area to the <textarea> element.
This method should be called after modifying the editor content through the DOM.

### value

Gets or sets the Editor value.

#### Example

    var editor = $("#editor").data("kendoEditor");
    
    // set value
    editor.value("<p>new content</p>");
    
    // get value
    var htmlValue = editor.value();

#### Parameters

##### value `String`

The value to set.

#### Returns

`String` The value of the Editor as HTML string.

## Events

### change

Fires when Editor is blurred and its content has changed.

#### Example

    function onChange(e) {
        // handle event
    }

### execute

Fires when an Editor command is executed.

#### Example

     $("#editor").kendoEditor({
         execute: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the Editor
     var editor = $("#editor").data("kendoEditor");
     // bind to the select event
     editor.bind("execute", function(e) {
         // handle event
     }

#### Event Data

##### e.name `String`

The name of the command

##### e.command `Object`

The command instance

### paste

Fires before when content is pasted in the Editor.

#### Example

     $("#editor").kendoEditor({
         paste: function(e) {
             // handle event
     });

#### To set after initialization

     // get a reference to the Editor
     var editor = $("#editor").data("kendoEditor");
     // bind to the select event
     editor.bind("paste", function(e) {
         // handle event
     }

#### Event Data

##### e.html `Object`

The pasted content

### select

Fires when the Editor selection has changed.

#### Example

     $("#editor").kendoEditor({
         select: function(e) {
             // handle event
         }
     });

#### To set after initialization

     // get a reference to the Editor
     var editor = $("#editor").data("kendoEditor");
     // bind to the select event
     editor.bind("select", function(e) {
         // handle event
     }