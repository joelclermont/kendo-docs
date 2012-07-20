---
title: kendo.data.ObservableArray
slug: fw-kendo.data.observablearray
tags: api,framework
publish: true
---

# kendo.data.ObservableArray

The `ObservableArray` wrap an existing Array object with change tracking capabilities. It is used by [Kendo MVVM](/getting-started/framework/mvvm/overview) and
the Kendo [DataSource](/getting-started/framework/datasource/overview).

## Configuration

To create a new `ObservableArray` use its constructor or the `kendo.observable` method.
### Creating a new ObservableArray

    var observableArray = new kendo.data.ObservableArray([{ name: "John Doe" }, { name: "Jane Doe" }]);
### Using the kendo.observable method

    var observable = kendo.observable({ people: [{ name: "John Doe" }, { name: "Jane Doe" }] });
    console.log(observable.people instanceof kendo.data.ObservableArray); // outputs "true"
> **Important**: The `ObservableArray` will wrap its items of complex type as `ObservableObject` instances.

### ObservableArray of complex and primitive type
    var complex = new kendo.data.ObservableArray([{ name: "John Doe" }, { name: "Jane Doe" }]);

    console.log(complex[0] instanceof kendo.data.ObservableObject); // outputs "true"

    var primitive = new kendo.data.ObservableArray(["John Doe", "Jane Doe"]);

    console.log(typeof (complex[0]) ); // outputs "string"
## Methods

### bind

Attaches an event handler for the specified event.

#### Example

    var array = new kendo.data.ObservableArray([1, 2]);

    array.bind("change", function(e) {
        console.log("changed");
    });

    array.push(3); // raises the "change" event and the handler outputs "changed"

#### Parameters

##### eventName `String`

The name of the event.

##### handler `Function`

The function which will be invoked when the event is raised.

### join

Joins all items of an `ObservableArray` into a string.

#### Syntax
    array.join(separator);

#### Parameters

##### separator `String`

Specifies the string to separate each item of the array.

### parent

Returns the parent `ObservableObject`. If the current `ObservableArray` is not nested
returns `undefined`.

#### Example

    var array = new kendo.data.ObservableArray([1, 2]);

    console.log(array.parent()); // outputs "undefined"

    var observable = kendo.observable({ numbers: [1, 2] });
    var numbers = observable.get("numbers");

    console.log(numbersperson.parent() === observable); // outputs "true"

### push

Appends the given items to the array and returns the new length of the array. Equivalent to the
[Array.prototype.push](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/push) method.
The new items are wrapped as `ObservableObject` if they are complex objects.

#### Syntax

    array.push(item1, ..., itemN);

#### Parameters

##### item1, ..., itemN

The item(s) to append to the array.

#### Append an item to an `ObservableArray`

    var array = new kendo.data.ObservableArray([{ name: "John Doe" }]);

    var length = array.push({ name: "Jane Doe" });

    console.log(length); // outputs "2"

    console.log(array[1] instanceof kendo.data.ObservableObject); // outputs "true"
    console.log(array[1].get("name")); // outputs "Jane Doe"

#### Append more than one item to an `ObservableArray`
    var array = new kendo.data.ObservableArray([ 1 ]);

    var length = array.push(2, 3);

    console.log(length); // outputs "3"

    console.log(array[1]); // outputs "2"
> **Important**: The `push` method raises the `change` event. The `action` field of the
event argument is set to `"add"`. The `items` field of the event argument is array that
contains the appended items.

### pop

Removes the last item from an array and returns that item. Equivalent to the
[Array.prototype.pop](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/pop) method.

#### Remove the last item from an `ObservableArray`

    var array = new kendo.data.ObservableArray([{ name: "John Doe" }]);

    var result = array.pop();

    console.log(array.length); // outputs "0"

    console.log(result.get("name")); // outputs "John Doe"

> **Important**: The `pop` method raises the `change` event. The `action` field of the
event argument is set to `"remove"`. The `items` field of the event argument is array that
contains the removed item.

### slice
Returns a one-level deep copy of a portion of an array. Equivalent to
[Array.prototype.slice](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/slice).
The result of the `slice` method is **not** an instance of `ObvservableArray`.
It is a regular JavaScript Array object.
> **Important:** The `slice` method does not modify the original `ObservableArray`.

#### Syntax
    array.slice(begin[, end])

#### Example

    var array = new kendo.data.ObservableArray([1, 2, 3]);
    var firstAndSecond = array.slice(0, 2);

    console.log(firstAndSecond); // outputs [1, 2]

#### Parameters

##### begin

Zero-based index at which to begin extraction.

##### end

Zero-based index at which to end extraction. If `end` is omitted, `slice` extracts to the
end of the sequence.


##Events

### change event

Raised when a field value is updated via the `set` method.

#### Example

    var observable = new kendo.data.ObservableArray({ name: "John Doe" });

    observable.bind("change", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.set("name", "Jane Doe"); // raises the "change" event and the handler outputs "name"

> The `change` event is raised **after** the field value is updated. Calling the `get` method from the event handler will return the new value.

#### Event Data

##### e.field `String`

The name of the field which has changed.

### get event

Raised when the `get` method is invoked.

#### Example

    var observable = new kendo.data.ObservableArray({ name: "John Doe" });

    observable.bind("get", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.get("name"); // raises the "get" event and the handler outputs "name"

#### Event Data

##### e.field `String`

The name of the field which is retrieved.

### set event

Raised when the `set` method is invoked.

#### Example

    var observable = new kendo.data.ObservableArray({ name: "John Doe" });

    observable.bind("set", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.set("name", "Jane Doe"); // raises the "set" event and the handler outputs "name"
> The `set` event is raised **before** the field value is updated. Calling the `get` method from the event handler will return the old value. Calling
`e.preventDefault` will prevent the update of the field and the `change` event will not be raised.

#### Event Data

##### e.field `String`

The name of the field which is retrieved.

##### e.value `Number|String|Data|Object`

The new value.

##### e.preventDefault `Function`

A function which may prevent the update of the value. Can be used to perform validation.

#### Perform validation by preventing the `set` event

    var observable = new kendo.data.ObservableArray({ name: "John Doe" });

    observable.bind("set", function(e) {
        if (e.field == "name") {
            if (!e.value) {
                // avoid emtpy value for the "name" field
                e.preventDefault();
            }
        }
    });

    observable.set("name", "Jane Doe");

