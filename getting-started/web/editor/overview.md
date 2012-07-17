---
title: Editor Overview
slug: editor-overview
tags: getting-started,web
publish: true
---

# Editor Overview

The Editor allows users to create rich text content by means of a WYSIWYG interfance. The generated widget value is an XHTML markup.

## Getting Started

### Creating an **Editor** from existing HTML element

      <textarea id="editor" rows="10" cols="30"></textarea>

### Initialize the Kendo Editor

      $(document).ready(function(){
          $("#editor").kendoEditor();
      });

## Configuring the Editor

The editor tools can be configured through the [`tools` configuration option](/api/web/editor#tools).

### Specifying a set of Editor tools

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

If no specific tools are defined, the Editor will create its default set of tools for text formatting.

## Specifying custom tools

The Editor functionality can be extended through custom tools, defined in the `tools` array alongside built-in tools.

### Adding a custom tool button

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

