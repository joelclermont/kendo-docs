---
title: kendo.data.ObservableObject
slug: fw-kendo.data.observableobject
tags: api,framework
publish: true
---

# kendo.data.ObservableObject

## Configuration

To create a new `ObservableObject` use its constructor or the `kendo.observable` method.
### Creating a new ObservableObject

    var observable = new kendo.data.ObservableObject( { name: "John Doe" });
### Using the kendo.observable method

    var observable = kendo.observable({ name: "John Doe" });

## Fields

### uid

The unique identifier of the `ObservableObject`.

#### Example
    var observable = new kendo.data.ObservableObject({ name: "John Doe" });
    console.log(observable.uid); // outputs a string in the form "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" where "x" is a number or letter

## Methods

### bind

Attaches an event handler for the specified event.

#### Example

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.bind("change", function(e) {
        console.log(e.field); // will output the changed field once the event is raised
    });

    observable.set("name", "Jane Doe"); // raises the "change" event and the handler outputs "name"

#### Parameters

##### eventName `String`

The name of the event.

##### handler `Function`

The function which will be invoked when the event is raised.

### get

Gets the value of the specified field.

#### Get the value of a field

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });
    var name = observable.get("name");

    console.log(name); //outputs "John Doe"

#### Get the value of a nested field

    var observable = new kendo.data.ObservableObject({ person: { name: "John Doe" } });

    var name = observable.get("person.name"); // use dot notation to denote nested fields

    console.log(name); //outputs "John Doe"

#### Parameters

##### name `String`

The name of the field whose value is going to be returned.

#### Returns

The value of the specified field.

### set

Sets the value of the specified field.

#### Set the value of a field

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.set("name", "Jane Doe"); // set the value

    console.log(observable.get("name")); //outputs the new value "Jane Doe"

#### Set the value of a nested field

    var observable = new kendo.data.ObservableObject({ person: { name: "John Doe" } });

    observable.set("person.name", "Jane Doe"); // set the value

    console.log(observable.get("person.name")); //outputs the new value "Jane Doe"
#### Parameters

##### name `String`

The name of the field whose value is going to be returned.

##### value `Number|String|Date|Object`

The new value of the field.

### toJSON

Creates a plain JavaScript object which contains all fields of the `ObservableObject`.

#### Example
    var observable = new kendo.data.ObservableObject({ person: { name: "John Doe" } });
    var json = observable.toJSON();

    console.log(JSON.stringify(json)); // outputs '{"person":{"name":"John Doe"}}'

#### Returns

An `Object` which contains only the fields of the `ObservableObject`.

## Events

### change

Raised when a field value is updated via the `set` method.

#### Example

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.bind("change", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.set("name", "Jane Doe"); // raises the "change" event and the handler outputs "name"

> The `change` event is raised **after** the field value is updated. This means that the `get` method will return the new value.

#### Event Data

##### e.field `String`

The name of the field which has changed.

### get

Raised when the `get` method is invoked.

#### Example

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.bind("get", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.get("name"); // raises the "get" event and the handler outputs "name"

#### Event Data

##### e.field `String`

The name of the field which is retrieved.

### set

Raised when the `set` method is invoked.

#### Example

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.bind("set", function(e) {
        console.log(e.field); // will output the field name when the event is raised
    });

    observable.set("name", "Jane Doe"); // raises the "set" event and the handler outputs "name"
> The `set` event is raised **before** the field value is updated. This means that the `get` method will return the old value. Calling
`e.preventDefault` will prevent the update of the field and the `change` event will not be raised.

#### Event Data

##### e.field `String`

The name of the field which is retrieved.

##### e.value `Number|String|Data|Object`

The new value.

##### e.preventDefault `Function`

A function which may prevent the update of the value. Can be used to perform validation.

    var observable = new kendo.data.ObservableObject({ name: "John Doe" });

    observable.bind("set", function(e) {
        if (e.field == "name") {
            if (!e.value) {
                // avoid emtpy value for the "name" field
                e.preventDefault();
            }
        }
    });

    observable.set("name", "Jane Doe");

