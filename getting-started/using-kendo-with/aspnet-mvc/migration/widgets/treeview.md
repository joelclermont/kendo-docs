---
title: TreeView
slug: treeview
publish: true
---

# Server-side API

### Remote data binding (Load On Demand)

#### Old

	<%= Html.Telerik().TreeView() 
	     .Name("TreeView") 
	     .DataBinding(dataBinding => dataBinding 
	         .Ajax().Select("_AjaxLoading", "TreeView") 
	     ) 
	 %>

#### New

	<%= Html.Telerik().TreeView() 
	     .Name("TreeView") 
	     .DataSource(source => { 
	           source.Read(read => 
	           { 
	               read.Action("_AjaxLoading ", "TreeView"); 
	           });  
	     }) 
	 %>

### Serializing Data

Data from the server should be serialized in the following JSON format:

	{ 
    	id: String, 
    	text: String, 
    	url: String, 
    	imageUrl: String, 
    	spriteCssClass: String, 
    	hasChildren: Boolean 
	}

All fields are optional (skipping the text field will show the item with the text “undefined”). The text/url/imageUrl/spriteCssClass field names can be changed through the DataTextField/DataUrlField/DataImageUrlField/DataSpriteCssClassField fluent methods:

	<%= Html.Kendo().TreeView() 
	     .Name("TreeView") 
	     .DataTextField("Name")
	     .DataSource(source => { 
	           source.Read(read => 
	           { 
	               read.Action("_AjaxLoading ", "TreeView"); 
	           });  
	     }) 
	 %>

The above code allows the items to be serialized in the following form:

	{ 
	    id: 2, 
	    Name: "Andrew", 
	    hasChildren: true 
	}

### Changing The Field That Posts The Item ID

By default, the **id** field will be posted to the server. To change the parameter name, you can use the Data handler: 

	<%= Html.Kendo().TreeView() 
	    .Name("treeview") 
	    .DataSource(dataSource => dataSource 
	        .Read(read => read 
	            .Action("Employees", "TreeView") 
	            .Data("addData") 
	        ) 
	    ) 
	%> 

	<script> 
	    function addData(data) { 
	        return { employeeId: data.id }; 
	    } 
	</script>

### Value Field

The value field is removed.  Depending on your use case, you can either:

- If the value was used for load on demand, use the **id** field.  The id will be inferred in the client-side datasource and will be used when making requests for more data.

-  If the value was used to store arbitrary data, serialize it in a data-* attribute through the item HtmlAttributes, or if a DataSource is used, access the additional data through the **dataItem** client-side method.

### CheckBox Support

The current checkbox support is limited to the functionality shown in the [templates demo](http://http://demos.kendoui.com/web/treeview/templates.html) (i.e. rendering only). Any data that needs to be passed to the server needs to be added in hidden fields with JavaScript, using the proper naming. The snippet below shows a possible approach for this:

	@(Html.Kendo().TreeView() 
	    .Name("treeview") 
	    .DataTextField("Name") 
	    .DataSource(dataSource => dataSource 
	        .Read(read => read 
	            .Action("Employees", "TreeView") 
	        ) 
	    ) 
	    .CheckboxTemplate("<input type='checkbox' />") 
	) 
	 
	<script id="itemInfoTemplate" type="text/kendo-ui-template"> 
	    # var name = "checkedEmployees"; /* modify this to change the argument name */ # 
	    # var arrayItem = name + "[" + index + "]"; # 
	    <input type="hidden" name="#= name #.Index" value="#= index #" /> 
	    <input type="hidden" name="#= arrayItem #.Id" value="#= item.id #" /> 
	    <input type="hidden" name="#= arrayItem #.Name" value="#= item.Name #" /> 
	</script> 
	     
	<script> 
	    function getNodeIndex(node) { 
	        return node.parentsUntil(".k-treeview", ".k-item").map(function() { 
	            return $(this).index(); 
	        }).toArray().reverse().join(":"); 
	    } 
	 
	    var itemInfoTemplate = kendo.template($("#itemInfoTemplate").html()); 
	 
	    var treeview = $("#treeview"); 
	 
	    treeview.on("change", ":checkbox", function(e) { 
	        var checkbox = $(this), 
	            dataItem = treeview.data("kendoTreeView").dataItem(checkbox.closest(".k-item")), 
	            index = getNodeIndex(checkbox); 
	 
	        checkbox.nextAll().remove(); 
	 
	        if (checkbox.is(":checked")) { 
	            checkbox.after(itemInfoTemplate({ 
	                item: dataItem, 
	                index: index 
	            })); 
	        } 
	    }); 
	</script>

Upcoming version of the MVC wrappers will introduce a more convenient way of handling checkboxes.

### Per-Item CheckBoxes

# Client-Side API Changes

#### MVC -> Kendo

##### ajaxRequest

Removed. Use **dataItem.dataSource.read()** (after obtaining the dataItem through **treeview.dataItem(node)**)

##### dataBind

Removed. Use **treeview.dataSource.read()**

##### disable

Removed. Use **treeview.enable(node, false)**

##### getItemText

Renamed. Use **treeview.text(node)**

##### getItemValue

Removed. See the [Value Field Is Removed](#value-field-is-removed) section of this document.

##### findByValue

Removed. See the [Value Field Is Removed](#value-field-is-removed) section of this document. An alternative is to use **treeview.findByUid** and access additional data in the related dataItem.

##### nodeCheck

Removed. See the [Checkbox Support](#checkbox-support) section of this document.

## Client-Side Events Changes

Apart from changing the event builders, the following changes have been introduced:

##### OnLoad

Removed. Use **$(document).ready()**

##### OnChecked

Removed. See the [Checkbox Support](#checkbox-support) section of this document.

##### OnDataBinding

Removed. Use the DataSource events

##### OnDataBound

Removed. Use the DataSource events

##### OnError

Removed. Use the DataSource events

##### OnNodeDragStart

Renamed. Use the **DragStart** event

##### OnNodeDragging

Renamed. Use the **Drag** event 

##### OnNodeDrop

Renamed. Use the **Drop** event

##### OnNodeDropped

Renamed. Use the **DragEnd** event