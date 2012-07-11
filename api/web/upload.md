---
title: kendo.ui.Upload
slug: web-kendo.ui.upload
tags: api,web
publish: true
---

# kendo.ui.Upload

## Description



An **Upload** uses progressive enhancement to deliver the best possible uploading experience to
users without requiring extra developer effort. Features highlights:


*   Asynchronous and synchronous (on form submit) file upload
*   Multiple file selection
*   Removing uploaded files
*   Progress tracking *
*   File drag-and-drop *
*   Cancelling upload in-progress *


(*) These features are automatically enabled if supported by the browser.

An **Upload** is a standards-based widget; no plug-ins required.

### Getting Started

#### 1\. Create a simple HTML form and input element of type "file"

    <!-- Kendo will automatically set the form enctype attribute to "multi-part/form-data" -->
    <form method="post" action="handler.php">
        <div>
            <input name="photos[]" id="photos" type="file" />
        </div>
    </form>

#### 2\. Initialize Upload with a jQuery selector

    $(document).ready(function() {
        $("#photos").kendoUpload();
    });

Note the array syntax in the input name; it is used to hint the upload handler to treat photos as an array.



Please consult the documentation of your specific server technology regarding the handling of uploaded files.


### See Also

[Upload Modes](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx)

### Accessing an Existing Upload


You can reference an existing **Upload** instance via
[jQuery.data()](http://api.jquery.com/jQuery.data/). Once a reference has been established, you can
use the API to control its behavior.

#### Accessing an existing Upload instance

    var upload = $("#upload").data("kendoUpload");

## Configuration

### async `Object`

Configures the ability to upload a file(s) in an asynchronous manner. Please refer to the
[async mode help topic](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async)
for more details.

### async.autoUpload `Boolean`*(default: true)*

The selected files will be uploaded immediately by default. You can change this behavior by setting
autoUpload to false.

### async.batch `Boolean`*(default: false)*

The selected files will be uploaded in separate requests, if this is supported by the browser.
You can change this behavior by setting batch to true.

### async.removeField `String`*(default: "fileNames")*

The name of the form field submitted to the Remove URL.

### async.removeUrl `String`

The URL of the handler responsible for removing uploaded files (if any). The handler must accept POST
requests containing one or more "fileNames" fields specifying the files to be deleted.

### async.removeVerb `String`*(default: "DELETE")*

The HTTP verb to be used by the remove action.

### async.saveField `String`

The name of the form field submitted to the save URL. The default value is the input name.

### async.saveUrl `String`

The URL of the handler that will receive the submitted files. The handler must accept POST requests
containing one or more fields with the same name as the original input name.

### enabled `Boolean`*(default: true)*

Enables (**true**) or disables (**false**) an **Upload**. A disabled
**Upload** may be re-enabled via enable().

### localization `Object`

Sets the strings rendered by the Upload.

### localization.cancel `String`

Sets the text of the cancel button text.

### localization.dropFilesHere `String`*(default: "drop files here to upload")*

Sets the drop zone hint.

### localization.remove `String`

Sets the text of the remove button text.

### localization.retry `String`

Sets the text of the retry button text.

### localization.select `String`

Sets the "Select..." button text.

### localization.statusFailed `String`

Sets the status message for failed uploads.

### localization.statusUploaded `String`

Sets the status message for uploaded files.

### localization.statusUploading `String`

Sets the status message for files that are being uploaded.

### localization.uploadSelectedFiles `String`

Sets the text of the "Upload files" button.

### multiple `Boolean`*(default: true)*

Enables (**true**) or disables (**false**) the ability to select multiple files.
If **false**, users will be able to select only one file at a time. Note: This option does not
limit the total number of uploaded files in an asynchronous configuration.

### showFileList `Boolean`*(default: true)*

Enables (**true**) or disables (**false**) the ability to display a file listing
for uploading a file(s). Disabling a file listing may be useful you wish to customize the UI; use the
client-side events to build your own UI.

## Methods

### disable

Disables the upload.

#### Example

    var upload = $("#upload").data("kendoUpload");

    // disables the upload
    upload.enable();

### enable

Enables the upload.

#### Example

    var upload = $("#upload").data("kendoUpload");

    // enables the upload
    upload.enable();

#### Parameters

##### enable ``



### toggle

Toggles the upload enabled state.

#### Example

    var upload = $("#upload").data("kendoUpload");

    // toggles the upload enabled state
    upload.toggle();

#### Parameters

##### enable `Boolean`

(Optional) The new enabled state.

## Events

### cancel

Fires when the upload has been cancelled while in progress.



Note: The cancel event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        cancel: onCancel
    });

    function onCancel(e) {
        // Array with information about the uploaded files
        var files = e.files;

        // Process the Cancel event
    }

#### Event Data

##### e.files `Array`

List of the files that were uploaded or removed . Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

### complete

Fires when all active uploads have completed either successfully or with errors.



Note: The complete event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        complete: onComplete
    });

    function onComplete(e) {
        // The upload is now idle
    }

### error

Fires when an upload / remove operation has failed.



Note: The error event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        error: onError
    });

    function onError(e) {
        // Array with information about the uploaded files
        var files = e.files;

        if (e.operation == "upload") {
            alert("Failed to uploaded " + files.length + " files");
        }
    }

#### Event Data

##### e.files `Array`

List of the files that were uploaded or removed . Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

##### e.operation `String`

- "upload" or "remove".

##### e.XMLHttpRequest `Object`

This is either the original XHR used for the operation or a stub containing:


*   responseText
*   status
*   statusText
Verify that this is an actual XHR before accessing any other fields.

### progress

Fires when upload progress data is available.


Note: The progress event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        progress: onProgress
    });

    function onProgress(e) {
        // Array with information about the uploaded files
        var files = e.files;

        console.log(e.percentComplete);
    }

#### Event Data

##### e.files `Array`

List of the files that are being uploaded. Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

##### percentComplete `Number`

Upload progress (0 - 100)

### remove

Fires when an uploaded file is about to be removed.
Cancelling the event will prevent the remove.

#### Example

    $("#photos").kendoUpload({
        // ...
        remove: onRemove
    });

    function onRemove(e) {
        // Array with information about the removed files
        var files = e.files;

        // Process the Remove event
        // Optionally cancel the remove operation by calling
        // e.preventDefault()
    }

#### Event Data

##### e.files `Array`

List of the files that were uploaded or removed . Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

##### data `Object`

Optional object that will be
sent to the save handler in the form of key/value pairs.

### select

Triggered when a file(s) is selected. Note: Cancelling this event will prevent the selection from
occurring.

#### Wire-up an event handler that triggered when a user selects a file(s)

    var onSelect = function(e) {
        $.each(e.files, function(index, value) {
            console.log("Name: " + value.name);
            console.log("Size: " + value.size + " bytes");
            console.log("Extension: " + value.extension);
        });
    };

    // initialize and configure an Upload widget with a select event handler
    $("#photos").kendoUpload({
        // ...
        select: onSelect
    });

#### Event Data

##### e.files `Array`

An array of the selected files.



*   name - the name of a selected file, including its extension
*   extension - the file extension of a selected file, including the leading dot (i.e. ".jpg")
*   size - the size (in bytes) of a selected file (null, if unavailable)
*   rawFile - an in-memory representation of a selected file

### success

Fires when an upload / remove operation has been completed successfully.



Note: The success event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        success: onSuccess
    });

    function onSuccess(e) {
        // Array with information about the uploaded files
        var files = e.files;

        if (e.operation == "upload") {
            alert("Successfully uploaded " + files.length + " files");
        }
    }

#### Event Data

##### e.files `Array`

List of the files that were uploaded or removed . Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

##### e.operation `String`

"upload" or "remove".

##### e.response `String`

the response object returned by the server.

##### e.XMLHttpRequest `Object`

This is either the original XHR used for the operation or a stub containing:


*   responseText
*   status
*   statusText
Verify that this is an actual XHR before accessing any other fields.

### upload

Fires when one or more files are about to be uploaded.
Cancelling the event will prevent the upload.



Note: The upload event fires only when the upload is in
[async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async).

#### Example

    $("#photos").kendoUpload({
        // ...
        upload: onUpload
    });

    function onUpload(e) {
        // Array with information about the uploaded files
        var files = e.files;

        // Check the extension of each file and abort the upload if it is not .jpg
        $.each(files, function() {
            if (this.extension != ".jpg") {
                alert("Only .jpg files can be uploaded")
                e.preventDefault();
            }
        });
    }

#### Event Data

##### e.files `Array`

List of the files that will be uploaded. Each file has:


*   name
*   extension - the file extension
        inlcuding the leading dot - ".jpg", ".png", etc.
*   size - the file size in bytes (null if not available)

##### data `Object`

Optional object that will be
sent to the save handler in the form of key/value pairs.
