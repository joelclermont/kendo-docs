---
title: Metadata
publish: true
---

Asynchronous uploading usually means that you lose the association betwen the files and the context that they originate from. 

Take an e-mail application for example. The save handler must associate the uploaded files to a particular message. 

The message and the file even might be processed on different servers in a load balancing or cloud computing scenario.

### Sending metadata to the save handler

1\. Add an input field for description. We will send its value to the save handler.
 <div class="reCodeBlock" style="border: 1px solid #7f9db9; overflow-y: auto;"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`&lt;``input` `type``=``"text"` `id``=``"fileDescription"` `/&gt;`</span></span></div> </div> 

2\. Declare a handler for the <a>upload event</a> and attach a data object to the passed event.
 <div class="reCodeBlock" style="border: 1px solid #7f9db9; overflow-y: auto;"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`function` `onUpload(e) {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`e.data = { fileDescription: $(``"#fileDescription"``).val() };`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`}`</span></span></div> </div> 

3\. Attach the event handler.

 <div class="reCodeBlock" style="border: 1px solid #7f9db9; overflow-y: auto;"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(``"#photos"``).kendoUpload({`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`async: {`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`saveUrl: ``"saveHandler.php"``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`removeUrl: ``"removeHandler.php"`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`},`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`upload: onUpload`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

4\. Process the file and the associated description

The description, and any other fields of the e.data object, will be serialized in the POST request.

Please consult the documentation of your server-side platform for instructions on how to read posted form fields.

### Receiving metadata from the save handler

The save handler can sometimes produce a result that needs to be routed back to the page.

1\. Build the response 

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`&lt;?php`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">&nbsp;</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`header(``'Content-Type: text/plain;'``);`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">&nbsp;</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$data` `= ``array``(``'foo'` `=&gt; ``'bar'``, ``'status'` `=&gt; ``'ok'``);`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">&nbsp;</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`echo` `json_encode(``$data``);`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">&nbsp;</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`?&gt;`</span></span></div> </div> 

The Upload requires the response to be in JSON format with Content-Type set to "text/plain". Any non-empty response that is not JSON will be treated as a server error.

2\. Declare a handler for the [success event](http://www.kendoui.com/documentation/ui-widgets/upload/events.aspx#success) and process the response

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`function` `onSuccess(e) {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`alert(``"Status: "` `+ e.response.status);`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`}`</span></span></div> </div> 

3\. Attach the event handler

 <div style="border: 1px solid #7f9db9; overflow-y: auto;" class="reCodeBlock"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`$(``"#photos"``).kendoUpload({`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`async: {`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`saveUrl: ``"saveHandler.php"``,`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 24px ! important;">`removeUrl: ``"removeHandler.php"`</span></span></div> <div style="background-color: #ffffff;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`},`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`success: onSuccess`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`});`</span></span></div> </div> 

The same approach is applicable for the remove handler as well. 

 