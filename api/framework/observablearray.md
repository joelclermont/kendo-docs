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

To create a new `ObservableArray`, use its constructor or the `kendo.observable` method.
### Creating a New ObservableArray

    var observableArray = new kendo.data.ObservableArray([{ name: "John Doe" }, { name: "Jane Doe" }]);
### Using the kendo.observable Method

    var observable = kendo.observable({ people: [{ name: "John Doe" }, { name: "Jane Doe" }] });
    console.log(observable.people instanceof kendo.data.ObservableArray); // outputs "true"
> **Important**: The `ObservableArray` will wrap its items of complex type as `ObservableObject` instances.

### ObservableArray of Complex and Primitive Type
    var complex = new kendo.data.ObservableArray([{ name: "John Doe" }, { name: "Jane Doe" }]);
    console.log(complex[0] instanceof kendo.data.ObservableObject); // outputs "true"

    var primitive = new kendo.data.ObservableArray(["John Doe", "Jane Doe"]);
    console.log(typeof (primitive[0]) ); // outputs "string"

## Fields

### length

An unsigned, 32-bit integer that specifies the number of items in an `ObservableArray`.

#### Example: Iterating Over ObservableArray
    var array = new kendo.data.ObservableArray([1, 2, 3]);

    for (var i = 0; i < array.length; i++) {
        console.log(array[i]); // outputs the current item
    }

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

Joins all items of an `ObservableArray` into a string. Equivalent of
[Array.prototype.join](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/join).

#### Syntax
    array.join(separator);

#### Parameters

##### separator `String`

Specifies the string to separate each item of the array. If omitted the array items are
separated with a comma (`,`)

#### Example
    var array = new kendo.data.ObservableArray([1, 2, 3]);

    console.log(array.join("-")); // outputs "1-2-3"

### parent

Returns the parent `ObservableObject`. If the current `ObservableArray` is not nested
returns `undefined`.

#### Example

    var array = new kendo.data.ObservableArray([1, 2]);

    console.log(array.parent()); // outputs "undefined"

    var observable = kendo.observable({ numbers: [1, 2] });
    var numbers = observable.get("numbers");

    console.log(numbersperson.parent() === observable); // outputs "true"

### pop

Removes the last item from an array and returns that item. Equivalent of
[Array.prototype.pop](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/pop).

#### Remove the last item from an `ObservableArray`

    var array = new kendo.data.ObservableArray([{ name: "John Doe" }]);

    var result = array.pop();

    console.log(array.length); // outputs "0"

    console.log(result.get("name")); // outputs "John Doe"

> **Important**: The `pop` method raises the `change` event. The `action` field of the
event argument is set to `"remove"`. The `items` field of the event argument is the array that
contains the removed item.

### push

Appends the given items to the array and returns the new length of the array. Equivalent of
[Array.prototype.push](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/push).
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
event argument is set to `"add"`. The `items` field of the event argument is the array that
contains the appended items.

### slice
Returns a one-level deep copy of a portion of an array. Equivalent of
[Array.prototype.slice](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/slice).
The result of the `slice` method is **not** an instance of `ObvservableArray`. It is a regular JavaScript Array object.
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

### splice

Changes an `ObservableArray`, by adding new items while removing old items. Equivalent of
[Array.prototype.splice](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/splice)

#### Syntax
    array.splice(index , howMany[, item1[, ...[, itemN]]])

#### Parameters

##### index `Number`
Index at which to start changing the array. If negative, will begin that many elements from the end.

##### howMany `Number`

An integer indicating the number of items to remove. If howMany is 0, no items are removed. In this case, you should specify at least one new item.

##### item1, ..., itemN
The items to add to the aray. If you don't specify any items, `splice` simply removes items from the array.

#### Returns

An `Array` containing the removed items. The result of the `splice` method is **not** an instance of `ObvservableArray`.

#### Example

    var sports = new kendo.data.ObservableArray(["football", "basketball", "volleyball"]);

    var removed = sports.splice(1, 1, "tennis", "hockey");

    console.log(removed); // outputs ["basketball"]

    console.log(sports); // outputs ["football", "tennis", "hockey", "volleyball"]


> **Important**: The `splice` method raises the `change` event once or twice depending on the change. The `action` field of the
event argument is set to `"add"` (if items are added) or `"remove` (if items are removed). The `items` field of the event argument is the array that
contains the appended items or removed items. In the above example the `change` event will be raised two times - first because "baseball" is removed and
second because "tennis" and "hockey" are added.

### shift
Removes the first item from an `ObvservableArray` and returns that item. Equivalent of
[Array.prototype.shift](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/shift).

#### Syntax
    array.shift();

#### Example
    var array = new kendo.data.ObservableArray([1, 2, 3]);

    var removed = array.shift();

    console.log(removed); // outputs "1"

    console.log(array.length); // outputs "2"

> **Important**: The `shift` method raises the `change` event. The `action` field of the
event argument is set to `"remove"`. The `items` field of the event argument is an array that
contains the removed item.

### toJSON

Returns a JavaScript Array which represents the contents of the `ObservableArray`.

#### Example
    var people = new kendo.data.ObservableArray([ { name: "John Doe" }, { name: "Jane Doe" }]);

    var json = people.toJSON();

    console.log(JSON.stringify(json)); // outputs [{"name":"John Doe"},{"name":"Jane Doe"}]

### unshift
Adds one or more items to the beginning of an `ObservableArray` and returns the new length.
Equivalent of [Array.prototype.unshift](http://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/unshift).

#### Syntax

    array.unshift(item1, ..., itemN);

#### Parameters

##### item1, ..., itemN
The items to add to the beginning of the `ObservableArray`.

#### Example
    var array = new kendo.data.ObservableArray([2, 3]);

    var result = array.unshift(0, 1);

    console.log(result); // outputs "4"

    console.log(result); // outputs [0, 1, 2, 3]

> **Important**: The `unshift` method raises the `change` event. The `action` field of the
event argument is set to `"add"`. The `items` field of the event argument is an array that
contains the new items.

## Events

### change

Raised when the items of the `ObservableArray` change in some way.

#### Event Data

##### e.action `String`

Specifies the type of change. Possible values are: `"add"`- items are added to the `ObservableArray`, `"itemchange"` - a field of an item changed, `"remove"` - items are removed from the `ObservableArray`.

##### e.index `Number`

The index at which items are removed or added. Set to `undefined` if `e.action` is `"itemchange"`.

##### e.items `Array`

The items which were changed.

##### e.field `String`

The name of the field of an item that changed. Available only when `e.action` is `"itemchange"`.

#### Example
    var array = new kendo.data.ObservableArray([1, 2, 3]);

    array.bind("change", function(e) {
        console.log(e.action, e.index, e.items);
    });

    array.push(4, 5); // outputs "add", 3, [4, 5]

    array.pop(); // outputs "remove", 4, [5]

    var people = new kendo.data.ObservableArray([{ name: "John Doe" }]);

    people.bind("change", function(e) {
        console.log(e.action, e.field, e.items[0].get("name"));
    });

    people[0].set("name", "Jane Doe"); // outputs "itemchange", "name", "Jane Doe"
