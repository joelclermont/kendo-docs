---
title: Walkthrough
slug: grid-walkthrough
publish: true
---

The Kendo UI Grid is a powerful piece of the Kendo UI framework and an essential part of almost any user interface.&nbsp; Kendo UI provides a grid component that is quick to setup and packed with features like sorting, grouping, paging and editing.

### Creating A Grid

To create a Kendo UI Grid, you begin with either an empty div, or an HTML table.&nbsp; If you create your grid with an empty div, you will be describing it’s layout in the JavaScript.&nbsp; If create the grid with a table, you can describe the grid layout entirely in the HTML of the table.

#### Grid Creation From A Div Element

First start with an empty div that has an ID.

  
    <span class="tag"><div</span><span class="pln"> </span><span class="atn">id</span><span class="pun">=</span><span class="atv">"grid"</span><span class="tag">></span> </div> 

Now turn the div into a grid by selecting the div with a jQuery selector, and calling the kendoGrid() function.&nbsp; Since the grid is being created off of an empty div, you must specify the column layout by passing an array of column definition objects to the columns property of the grid.
  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; columns</span><span class="pun">:</span><span class="pln"> </span><span class="pun">[</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> title</span><span class="pun">:</span><span class="pln"> </span><span class="str">"First Name"</span><span class="pun">,</span><span class="pln"> field</span><span class="pun">:</span><span class="pln"> </span><span class="str">"firstName"</span><span class="pln"> </span><span class="pun">},</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">{</span><span class="pln"> title</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Last Name"</span><span class="pun">,</span><span class="pln"> field</span><span class="pun">:</span><span class="pln"> </span><span class="str">"lastName"</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">{</span><span class="pln"> title</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Email"</span><span class="pun">,</span><span class="pln"> field</span><span class="pun">:</span><span class="pln"> </span><span class="str">"email"</span><span class="pln"> </span><span class="pun">}</span><span class="pln"> </span><span class="pun">]</span><span class="pln">
    </span><span class="pun">});</span>  

<span style="background-color: #ffffff;">Each column object has the following properties:</span>

1.  **title**: This is the text you want to appear as the column header
2.  **field**: The field in the data set that this column should be bound to.
3.  **template**: You can specify a template for the grid column to display instead of plain text.
4.  **width**: The desired width of the column. 

#### Grid Creation From An HTML Table

Add an HTML table.&nbsp; Specify the table header.&nbsp; Each of _th_ elements you specify will become a column and the text will become the column header.&nbsp;
  
    <span class="tag"><table</span><span class="pln"> </span><span class="atn">id</span><span class="pun">=</span><span class="atv">"grid"</span><span class="tag">></span><span class="pln"> &nbsp; &nbsp; 
    </span><span style="white-space: pre;" class="Apple-tab-span"><span class="pln">&nbsp;</span></span><span class="tag"><thead></span><span class="pln"> &nbsp; &nbsp; &nbsp; &nbsp; 
    </span><span style="white-space: pre;" class="Apple-tab-span"><span class="pln">&nbsp;</span></span><span class="tag"><th</span><span class="pln"> </span><span class="atn">data-field</span><span class="pun">=</span><span class="atv">"firstName"</span><span class="tag">></span><span class="pln">First Name</span><span class="tag"></th></span><span class="pln"> &nbsp; &nbsp; &nbsp; &nbsp; 
    </span><span style="white-space: pre;" class="Apple-tab-span"><span class="pln">&nbsp;</span></span><span class="tag"><th</span><span class="pln"> </span><span class="atn">data-field</span><span class="pun">=</span><span class="atv">"lastName"</span><span class="tag">></span><span class="pln">Last Name</span><span class="tag"></th></span><span class="pln"> &nbsp; &nbsp; &nbsp; &nbsp; 
    </span><span style="white-space: pre;" class="Apple-tab-span"><span class="pln">&nbsp;</span></span><span class="tag"><th</span><span class="pln"> </span><span class="atn">data-field</span><span class="pun">=</span><span class="atv">"email"</span><span class="tag">></span><span class="pln">Email</span><span class="tag"></th></span><span class="pln"> &nbsp; &nbsp; 
    </span><span style="white-space: pre;" class="Apple-tab-span"><span class="pln">&nbsp;</span></span><span class="tag"></thead></span><span class="pln">
    </span><span class="tag"></table></span><span class="pln">
    </span>  

The table can now describe the entire structure of the grid.&nbsp; The field that the column is bound to in the data set is specified in the _data-field_<span style="white-space: normal; font-family: times;"> attribute of each </span>_th_element.&nbsp; Additionally, row templates can be defined in the table structure.

Since the layout of the grid is defined by the HTML it’s only necessary to call the kendoGrid() function to create a grid.

  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">();</span>  

At this point, either way the grid was created you will have an empty grid.&nbsp; It will look more or less like this depending on how you have themed your download.

<span style="font-weight: bold; font-size: 24px; color: #e36c0a;">![Initialized Grid](/Libraries/Blog_Images/grid1_3.sflb.ashx)
 </span>

### Data Binding - Local

The next step is to bind the grid to data.&nbsp; The grid can be bound to local data very simply by specifying the _data _attribute of the kendoGrid object.

  
    <span class="kwd">var</span><span class="pln"> people </span><span class="pun">=</span><span class="pln"> </span><span class="pun">[</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> firstName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"John"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;lastName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Smith"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;email</span><span class="pun">:</span><span class="pln"> </span><span class="str">"john.smith@kendoui.com"</span><span class="pln"> </span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">{</span><span class="pln"> firstName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Jane"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;lastName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Smith"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;email</span><span class="pun">:</span><span class="pln"> </span><span class="str">"jane.smith@kendoui.com"</span><span class="pln"> </span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">{</span><span class="pln"> firstName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Josh"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;lastName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Davis"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;email</span><span class="pun">:</span><span class="pln"> </span><span class="str">"josh.davis@kendoui.com"</span><span class="pln"> </span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">{</span><span class="pln"> firstName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Cindy"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;lastName</span><span class="pun">:</span><span class="pln"> </span><span class="str">"Jones"</span><span class="pun">,</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;email</span><span class="pun">:</span><span class="pln"> </span><span class="str">"cindy.jones@kendoui.com"</span><span class="pln"> </span><span class="pun">}</span><span class="pln"> </span><span class="pun">];</span><span class="pln">
    
    &nbsp;$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> people
    &nbsp;</span><span class="pun">});</span>  

![Grid Bound To Local Data](/Libraries/Blog_Images/grid2_1.sflb.ashx)

### Data Binding – Remote

The grid can bound to remote data by specifying the dataSource property.&nbsp; The data source can either be created outside of the grid or passed in.&nbsp; If you have multiple widgets bound to the same set of data, you would create the data source as an object that you could reference in different widgets.&nbsp; If the grid is the only item bound to the data, it makes more sense to simply create it inline.
  
    <span class="pln">&nbsp;$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">"/Home/People.json"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    </span><span class="pun">});</span>  

<span style="font-weight: bold; background-color: #ffffff;">Auto Binding</span>

The grid is set to autobind to data by default, meaning it will cause the data source to query as soon as it’s loaded and data will be loaded into the grid.&nbsp; This can be disabled by setting the _autoBind _property of the grid to _false_.

  
    <span class="pln">autoBind</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">false</span>  

## Grid Size

By default, the grid will expand to fit the width and height of its container and contents.&nbsp; You can control the height of the grid by specifying a static pixel value.

  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">"/Home/People.json"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;height</span><span class="pun">:</span><span class="pln"> </span><span class="lit">100</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

![Grid With Fixed Height And Scrolling](/Libraries/Blog_Images/grid3_1.sflb.ashx)

Setting CSS width properties for the grid itself, or the parent container of the grid controls the width of the grid.

#### Making the Grid 100% high and auto resizable

 In order to configure the Grid to be 100% high and resize together with its parent element on browser window resize, the following Javascript code must be used:
  
    <span class="js-keyword">function </span><span class="js-variable">resizeGrid</span><span class="js-punctuation">(</span><span class="js-punctuation">) </span><span class="js-punctuation">{</span>
    <span class="whitespace">&nbsp; &nbsp;&nbsp;</span><span class="js-keyword">var </span><span class="js-variabledef">gridElement </span><span class="js-operator">= </span><span class="js-variable">$</span><span class="js-punctuation">(</span><span class="js-string">"#grid"</span><span class="js-punctuation">)</span><span class="js-punctuation">,</span>
    <span class="whitespace">&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span><span class="js-variabledef">newHeight </span><span class="js-operator">= </span><span class="js-localvariable">gridElement</span><span class="js-punctuation">.</span><span class="js-property">innerHeight</span><span class="js-punctuation">(</span><span class="js-punctuation">)</span><span class="js-punctuation">,</span>
    <span class="whitespace">&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span><span class="js-variabledef">otherElements </span><span class="js-operator">= </span><span class="js-localvariable">gridElement</span><span class="js-punctuation">.</span><span class="js-property">children</span><span class="js-punctuation">(</span><span class="js-punctuation">)</span><span class="js-punctuation">.</span><span class="js-property">not</span><span class="js-punctuation">(</span><span class="js-string">".k-grid-content"</span><span class="js-punctuation">)</span><span class="js-punctuation">,</span>
    <span class="whitespace">&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span><span class="js-variabledef">otherElementsHeight </span><span class="js-operator">= </span><span class="js-atom">0</span><span class="js-punctuation">;</span>
    <span class="whitespace">&nbsp; &nbsp;&nbsp;</span><span class="js-localvariable">otherElements</span><span class="js-punctuation">.</span><span class="js-property">each</span><span class="js-punctuation">(</span><span class="js-keyword">function</span><span class="js-punctuation">(</span><span class="js-punctuation">)</span><span class="js-punctuation">{</span>
    <span class="whitespace">&nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span><span class="js-localvariable">otherElementsHeight </span><span class="js-operator">+= </span><span class="js-variable">$</span><span class="js-punctuation">(</span><span class="js-localvariable">this</span><span class="js-punctuation">)</span><span class="js-punctuation">.</span><span class="js-property">outerHeight</span><span class="js-punctuation">(</span><span class="js-punctuation">)</span><span class="js-punctuation">;</span>
    <span class="whitespace">&nbsp; &nbsp;&nbsp;</span><span class="js-punctuation">}</span><span class="js-punctuation">)</span><span class="js-punctuation">;</span>
    <span class="whitespace">&nbsp; &nbsp;&nbsp;</span><span class="js-localvariable">gridElement</span><span class="js-punctuation">.</span><span class="js-property">children</span><span class="js-punctuation">(</span><span class="js-string">".k-grid-content"</span><span class="js-punctuation">)</span><span class="js-punctuation">.</span><span class="js-property">height</span><span class="js-punctuation">(</span><span class="js-localvariable">newHeight </span><span class="js-operator">- </span><span class="js-localvariable">otherElementsHeight</span><span class="js-punctuation">)</span><span class="js-punctuation">;</span>
    <span class="js-punctuation">}</span>  

The above script should be executed as a window resize event handler. The Grid &lt;div&gt; should have a 100% height style applied and its default borders should be removed. Note that elements with percentage height require a parent element with an explicit height.

## Features

#### Scrolling

Scrolling is enabled by default on the grid, but can be turned off by setting the _scrollable_ attribute to false.&nbsp; There are the other available settings for _scrollable_.

  

#### Default: Enable scrolling in the grid in the grid
 
    <span class="pln">scrollable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp;</span>   

#### Disable scrolling in the grid
 
    <span class="pln">scrollable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">false</span>  

Virtual Scrolling will load in data from the remote data source as you scroll down the grid
  

#### Enable virtual scrolling
 
    <span class="pln">scrollable</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; virtual</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    </span><span class="pun">}</span>  

  

#### Virtual scrolling disabled but regular scrolling still enabled
 
    <span class="pln">scrollable</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; virtual</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">false</span><span class="pln">
    </span><span class="pun">}</span>  

#### Selection 

Selection can be enabled in the grid simply by setting the _selectable_ property to true.

This will by default enable single row selection in the grid.

  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">"/Home/People.json"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;selectable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

![Grid With Row Selection Enabled](/Libraries/Blog_Images/grid4_1.sflb.ashx)

The _selectable _property can also be set to the following values:

  

#### Default. Enables single row selection
 
    <span class="pln">selectable</span><span class="pun">:</span><span class="pln"> </span><span class="str">"row"</span>   

#### Enable selection of individual cells within the grid.
 
    <span class="pln">selectable</span><span class="pun">:</span><span class="pln"> </span><span class="str">"cell"</span>   

#### Allow users to select multiple rows in the grid.
 
    <span class="pln">selectable</span><span class="pun">:</span><span class="pln"> </span><span class="str">"multiple, row"</span>   

#### Enables multiple cell selection.
 
    <span class="pln">selectable</span><span class="pun">:</span><span class="pln"> </span><span class="str">"multiple, cell"</span>  

When _multiple_ selection is enabled, it is possible to select multiple rows/cells by dragging the mouse cursor to select them similar to the way you would select a block of text.

#### Paging

The paging setting within the grid is controlled by the _pageable_ attribute.&nbsp; The grid will additionally need to know how many records to display on each page and the total number of records in the data set.&nbsp; Specify the _pageSize _&nbsp;on the data source and the field in the dataset that will contain the total count of records.

  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">'/Home/People.json'</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;total</span><span class="pun">:</span><span class="pln"> </span><span class="str">"count"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;pageSize</span><span class="pun">:</span><span class="pln"> </span><span class="lit">2</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;selectable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp; &nbsp; &nbsp;pageable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

It is often preferred to do paging operations on the server to keep from including too much data in the HTML, which can slow down page performance.&nbsp; To accomplish this, set the _serverPaging _attribute on the data source to true.

In the instance that you decide to use server paging, you must be prepared to handle the requests to the server and respond appropriately.&nbsp; The data source will send the following default parameters to the server when _serverPaging _is enabled.

**top**: The number of records to send back in the response.

**skip**: The number of records to skip from the start of the dataset.

For instance, if you wanted page 3 of a 60 record dataset at 10 records per page, the grid would send _skip_: 20, _top_: 10.&nbsp; 

#### Grouping

Setting the _groupable_ property to true turns on grouping in the grid.&nbsp; This property can only be set to true or false.&nbsp; By default, it is set to false.

Once grouping is enabled, a new area will be exposed in the header informing you to drop a column there to group by that column.&nbsp; It is possible to group by multiple columns simply by dragging a second column onto the grouping header.
  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">'/Home/People.json'</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;selectable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;groupable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

![Grid With Grouping Enabled](/Libraries/Blog_Images/grid5_1.sflb.ashx)

![Grid Grouped By Last Name](/Libraries/Blog_Images/grid6_1.sflb.ashx)

You can additionally sort the grouping by clicking on the grouping tab.&nbsp; In this example, clicking on “lastName” will sort the grouping descending.&nbsp; Clicking it again will toggle to ascending.&nbsp; Each of the individual groups themselves can be toggled from expanded to collapsed by clicking on the arrow next to the respective header grouping.

#### Sorting

Sorting is supported in two formats: either single-column sorting, or multi-column sorting.&nbsp; To enable single column sorting, set the _sortable_ property of the grid to true.&nbsp; This will enable the default single column sorting.&nbsp;
  
    <span class="pln">$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">'/Home/People.json'</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;selectable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;groupable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;sortable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

![Grid With Sorting Enabled](/Libraries/Blog_Images/grid7_1.sflb.ashx)

The sortable attribute also has the following settings:
  

#### Enable single column sorting
 
    <span class="pln">sortable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span>   

#### Enable multi-column sorting
 
    <span class="pln">sortable</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
        mode</span><span class="pun">:</span><span class="pln"> </span><span class="str">"multiple"</span><span class="pln">
    </span><span class="pun">}</span>  

Sorting is also a function that can be pushed to the server for increased performance.&nbsp; This is done via the data source itself and setting the _serverSorting _property on the data source to _true_.&nbsp; When you delegate sorting to the server, you need to be prepared to receive the default parameter, which is _orderBy_.&nbsp; This field will contain the field name of the column to sort by in the dataset.

If you are also doing paging operations on the server, you will need to be ready to handle the _top_ and _skip_ options as well in your query.

#### Keyboard Navigation

Keyboard navigation within the grid is supported by the _navigatable_ property.&nbsp; When set to true, you will be able to move through the grid using the arrow keys after you have initially selected a row/cell.&nbsp;&nbsp; The navigation occurs at a cell level regardless of what _selectable _mode is specified.&nbsp; The current row/cell will be selected when the space bar is pressed.

  

#### Enable keyboard navigation
 
    <span class="pln">navigatable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span>  

## Applying Templates To Cells

Using templates within either a script tag, or the template property on the column object if the grid is being initialized from a div can format each cell in the grid.

In this example, a template is used to format the email address as a hyperlink by using a template declared in a script block
  
    <span class="pun"><</span><span class="pln">script id</span><span class="pun">=</span><span class="str">"template"</span><span class="pln"> type</span><span class="pun">=</span><span class="str">"text/x-kendo-tmpl"</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; </span><span class="pun"><</span><span class="pln">tr</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun"><</span><span class="pln">td</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun">#=</span><span class="pln"> firstName </span><span class="pun">#</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun"><</span><span class="str">/td>
    &nbsp; &nbsp; &nbsp; &nbsp; <td>
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; #= lastName #
    &nbsp; &nbsp; &nbsp; &nbsp; </</span><span class="pln">td</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun"><</span><span class="pln">td</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun"><</span><span class="pln">a href</span><span class="pun">=</span><span class="str">"mailto:#= email #"</span><span class="pun">>#=</span><span class="pln"> email </span><span class="pun">#</</span><span class="pln">a</span><span class="pun">></span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; </span><span class="pun"><</span><span class="str">/td>
    &nbsp; &nbsp; </</span><span class="pln">tr</span><span class="pun">></span><span class="pln">
    </span><span class="pun"></</span><span class="pln">script</span><span class="pun">></span>  

This is then specified as the template for each row by passing it in to the _rowTemplate _property on the grid and initializing it with the kendo.template function.
  
    <span class="pln">&nbsp;$</span><span class="pun">(</span><span class="str">"#grid"</span><span class="pun">).</span><span class="pln">kendoGrid</span><span class="pun">({</span><span class="pln">
    &nbsp; &nbsp; &nbsp;dataSource</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln"> 
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;transport</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;read</span><span class="pun">:</span><span class="pln"> </span><span class="str">'/Home/People.json'</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;schema</span><span class="pun">:</span><span class="pln"> </span><span class="pun">{</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;data</span><span class="pun">:</span><span class="pln"> </span><span class="str">"data"</span><span class="pln">
    &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="pun">}</span><span class="pln">
    &nbsp; &nbsp; &nbsp;</span><span class="pun">},</span><span class="pln">
    &nbsp; &nbsp; &nbsp;selectable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">false</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;groupable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;sortable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;navigatable</span><span class="pun">:</span><span class="pln"> </span><span class="kwd">true</span><span class="pun">,</span><span class="pln">
    &nbsp; &nbsp; &nbsp;rowTemplate</span><span class="pun">:</span><span class="pln"> kendo</span><span class="pun">.</span><span class="pln">template</span><span class="pun">(</span><span class="pln">$</span><span class="pun">(</span><span class="str">"#template"</span><span class="pun">).</span><span class="pln">html</span><span class="pun">())</span><span class="pln">
    &nbsp;</span><span class="pun">});</span>  

Now the email address is an interactive hyperlink&nbsp; that will open a new email message.

![Grid With Row Template](/Libraries/Blog_Images/grid8_1.sflb.ashx)