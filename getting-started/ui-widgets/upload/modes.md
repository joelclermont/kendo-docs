---
title: Modes
publish: true
---

 

The Upload supports two modes of operation - synchronous and asynchronous.

 <a name="sync"></a> 

### Synchronous mode

From a developer's perspective an Upload in sync mode&nbsp;behaves much like a regular file input.&nbsp;The selected files will be uploaded when the form is submitted.

The users benefit from the ability to select a variable number of files. This feature does not require the browser to support multiple file selection.

![](/Libraries/Documentation/upload-sync.sflb.ashx)

The Upload is initialized from an existing file input placed in a form.

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`&lt;``form`&nbsp;`method``=``"post"`&nbsp;`action``=``"handler.php"``&gt;`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`&lt;``div``&gt;`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`&lt;``input`&nbsp;`name``=``"photos[]"`&nbsp;`id``=``"photos"`&nbsp;`type``=``"file"`&nbsp;`/&gt;`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`&lt;/``div``&gt;`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`&lt;/``form``&gt;`</span></span></div> </div> 

Note the array syntax in the input name. It is used to hint the upload handler to treat photos as an array.

Invoke the kendoUpload method for each such input:

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(document).ready(``function``() {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`$(``"#photos"``).kendoUpload();`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

Please consult the documentation of your specific server technology regarding the handling of uploaded files.

 <a name="async"></a> 

### <span>Asynchronous mode</span>

In this mode the Upload requires dedicated server handlers to store and&nbsp;remove&nbsp;uploaded files. Files are uploaded immediately or, optionally, after user confirmation. The upload request is executed out-of-band without interrupting the page flow.

![](/Libraries/Documentation/upload-async.sflb.ashx)

The async mode is implemented using the HTML5 File API. The upload will gracefully degrade and continue to function in legacy browsers using a hidden IFRAME.

Start by creating&nbsp;a simple HTML input of type "file" (no form is required):

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span style="margin-left: 0px ! important;">`&lt;``input`&nbsp;`name``=``"photos[]"`&nbsp;`id``=``"photos"`&nbsp;`type``=``"file"`&nbsp;`/&gt;`</span></div> </div> 

Initialize Upload and configure async upload end-points:
 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(``"#photos"``).kendoUpload({`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`async: {`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`saveUrl: ``"saveHandler.php"``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`removeUrl: ``"removeHandler.php"``,`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`removeField: ``"fileNames[]"`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`}`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

We use the familiar array syntax for the field name in order to hint the upload handler to treat "photos" as an array.

#### Save handler
 <div>The save handler should accept POST requests. The requests will contain one or more files with the same name as the input, in this case "photos[]".

The handler should return either:</div> 

*   An empty response to signify success.
*   A JSON string&nbsp;with "text/plain" content encoding. The de-serialized object is available in the&nbsp;**success&nbsp;**event handler.
*   Any other response to signify failure. 

#### Remove handler

The remove handler should accept DELETE requests (configurable). The requests will contain one or more text fields with name "fileNames". In this case, we change it to "fileNames[]" using the removeField option.

The handler should return either:

*   An empty response to signify success.
*   A JSON string&nbsp;with "text/plain" content encoding. The de-serialized object is available in the&nbsp;**success&nbsp;**event handler.
*   Any other response to signify failure. 

#### Asynchronous mode fallback

The Upload has a fallback mechanism when it is placed inside a form and is configured for asynchronous operation. Any files that were not fully uploaded will be sent as part of the form when the user submits it. This ensures that no files will be lost, even if you do not take any special measures to block the submit button during upload.

&nbsp;&nbsp;

You have to handle the uploaded files both in the save handler and in the form submit action, as in synchronous mode.

### See also

See the&nbsp;[Configuration](http://www.kendoui.com/documentation/ui-widgets/upload/configuration.aspx)&nbsp;help topic for a full list of options.