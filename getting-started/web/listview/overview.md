---
title: ListView Overview
slug: getting-started.web.listview
tags: getting-started,web
publish: true
---

# ListView Overview

The ListView is designed to give your the freedom to specify custom type of layout
for the items displayed in the control. It can be bound to local JSON data or to
remote data using the Kendo DataSource component.


## Getting Started

### Creating a **ListView** from existing HTML element

      <ul id="listView"></ul>

### Initialize the Kendo ListView

      $(document).ready(function() {
          $("#listView").kendoListView({
              template: "<li>${FirstName} ${LastName}</li>",
              dataSource: {
                  data: [
                      {
                          FirstName: "Joe",
                          LastName: "Smith"
                      },
                      {
                          FirstName: "Jane",
                          LastName: "Smith"
                  }]
              }
          });
      });

## Configuring ListView Behavior

Kendo ListView supports paging, selection, navigation, editing. Configuring any of
these ListView behaviors is done using simple boolean configuration options. For
example, the follow snippet shows how to enable all of these behaviors.

### Enabling ListView paging, selection, navigation and editing

      $(document).ready(function() {
          $("#listView").kendoListView({
             pageable: true,
             selectable: true,
             navigatable: true,
             editable: true,
             template: "<li>${FirstName}</li>",
             editTemplate: '<li><input type="text" data-bind="value:FirstName" name="FirstName" required="required"/></li>'
          });
      });

By default, paging, selection, navigation and editing are **disabled**.

