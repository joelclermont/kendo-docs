---
title: Drag and drop
publish: true
---

Users can select files by dropping them over the Upload.

This feature is only available in [async mode](http://www.kendoui.com/documentation/ui-widgets/upload/modes.aspx#async) and requires a supported browser.

### Uploading files with drag &amp; drop

1\. The drop zone will appear when a file is dragged over the browser window.

&nbsp;![](/Libraries/Documentation/upload-dd1.sflb.ashx)

2\. The drop zone will be highlighted when the mouse is over it. 

![](/Libraries/Documentation/upload-dd2.sflb.ashx)

3.&nbsp; Releasing the file over the drop zone will add it to the upload queue.

![](/Libraries/Documentation/upload-dd3.sflb.ashx)&nbsp;

### &nbsp;Drop zone visibility

The drop zone is not visible by default. You can override this behavior with the following CSS rules:

 <div class="reCodeBlock" style="border: 1px solid #7f9db9; overflow-y: auto;"> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`div.t-dropzone {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`border``: ``1px` `solid` `#c5c5c5``; ``/* Default skin */`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`}`</span></span></div> <div style="background-color: #f8f8f8;"><span><span style="margin-left: 0px ! important;">&nbsp;</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`div.t-dropzone em {`</span></span></div> <div style="background-color: #f8f8f8;"><span>`&nbsp;&nbsp;&nbsp;&nbsp;`<span style="margin-left: 12px ! important;">`visibility``: ``visible``;`</span></span></div> <div style="background-color: #ffffff;"><span><span style="margin-left: 0px ! important;">`}`</span></span></div> </div>