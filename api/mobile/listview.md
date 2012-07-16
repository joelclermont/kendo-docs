---
title: kendo.mobile.ui.ListView
slug: mobile-kendo.mobile.ui.listview
tags: api,mobile
publish: true
---

# kendo.mobile.ui.ListView

## Configuration

### appendOnRefresh `Boolean`*(default: false)*

 Used in combination with pullToRefresh. If set to true, newly loaded data will be appended on top when refershing.

### autoBind `Boolean`*(default: true)*

 Indicates whether the listview will call read on the DataSource initially.

### dataSource `kendo.data.DataSource | Object`

Instance of DataSource or the data that the mobile ListView will be bound to.

### endlessScroll `Boolean`*(default: false)*

 If set to true, the listview gets the next page of data when the user scrolls near the bottom of the view.

### fixedHeaders `Boolean`*(default: false)*

 If set to true, the group headers will persist their position when the user scrolls through the listview. Applicable only when the type is set to group, or when binding to grouped datasource.

### headerTemplate `String`*(default: #:value#)*

 The header item template (applicable when the type is set to group).

### loadMore `Boolean`*(default: false)*

 If set to true, a button is rendered at the bottom of the listview, which fetch the next page of data when tapped.

### loadMoreText `String`*(default: "Press to load more")*

 The text of the rendered load-more button (applies only if loadMore is set to true).

### pullTemplate `String`*(default: "Pull to refresh")*

 The message template displayed when the user pulls the listView. Applicable only when pullToRefresh is set to true.

### pullToRefresh `Boolean`*(default: false)*

 If set to true, the listview will reload its data when the user pulls the view over the top limit.

### refreshTemplate `String`*(default: "Refreshing")*

 The message template displayed during the refresh. Applicable only when pullToRefresh is set to true.

### releaseTemplate `String`*(default: "Release to refresh")*

 The message template indicating that pullToRefresh will occur. Applicable only when pullToRefresh is set to true.

### scrollTreshold `String`*(default: 30)*

 The distance to the bottom in pixels, after which the listview will start fetching the next page. Applicable only when endlessScroll is set to true.

### style `String`

The style of the control. Can be either empty string(""), or inset.

### template `String`*(default: #:data#)*

 The item template.

### type `String`

The type of the control. Can be either `flat` (default) or group. Determined automatically in databound mode.

## Methods

### items

Get the listview DOM element items

#### Returns

`jQuery` The listview DOM element items

### refresh

Repaints the listview (works only in databound mode).

#### Example

    // get a reference to the mobile listview widget
    var listView = $("#listView").data("kendoMobileListView");
    // refreshes the listview
    listview.refresh();

#### Parameters

##### e ``



## Events

### click

Fires when item is tapped.

#### Handling button clicks

    <ul data-role="listview" id="foo" data-click="listViewClick">
        <li><a data-role="button" data-name="bar">Bar button</a> | <a data-role="button" data-name="baz">Baz button</a></li>
    </ul>
    
    <script>
     function listViewClick(e) {
         console.log(e.button); // Kendo mobile Button instance
     }
    </script>

#### Accessing dataItem in event

    <ul id="foo"></ul>
    
    <script>
     $("#foo").kendoMobileListView({
        dataSource: new kendo.data.DataSource({
             data:   [{title: "foo"}, {title: "bar"}]
        }),
    
        click: function(e) {
             console.log(e.dataItem.title);
        }
     });
    </script>

#### Event Data

##### e.item `jQuery`

The selected list item.

##### e.target `jQuery`

The tapped DOM element.

##### e.dataItem `Object`

The corresponding dataItem associated with the item (available in databound mode only).
Note: The dataItem must be from a non-primitive type (Object).

##### e.button `kendo.mobile.ui.Button`

The tapped Kendo mobile Button (if present).
