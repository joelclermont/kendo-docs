---
title: Introduction
publish: true
---

### What is Kendo UI

[Kendo UI ](http://www.kendoui.com/) is an HTML5, [jQuery](http://jquery.com)-based framework for building modern web apps. The framework features more than a dozen UI components,
including a Grid and Chart, and all of the tools needed for a HTML5 app development, such as Data Binding, Templating, Drag-and-Drop API, and more.
When you start building with Kendo UI, you have the core pieces you need:

*   UI widgets
*   Client-side DataSource
*   High-performance Templates
*   Data Binding
*   Drag-and-Drop API
*   Animations
*   Built-in touch support 

There’s no need to manually assemble a full framework for HTML app development; Kendo UI provides all the building blocks, designed to seamlessly work together. It is not only UI, but much more.

#### Built for Performance

Every aspect of Kendo UI has been built to deliver performance before providing a laundry list of features. No shortcuts have been made to artificially inflate the Kendo UI feature set.&nbsp;

### 

#### Built for Real World Use

Even though Kendo UI is built to leverage the power of new HTML5, CSS3, and JavaScript technologies, it is also built for the realities of a world that does not universally support HTML5 today. In fact, Kendo helps developers adopt the latest in web standards faster by automatically handling the support for older browsers. It does for HTML5 application development what jQuery does for JavaScript.

### Download

You can download Kendo UI [here](/download)

### Contents of Kendo UI zip file distribution:

*   **/examples** - Kendo UI quick start demos
*   **/js** - Kendo UI minified javascript files
*   **/source** - Kendo UI complete source code
*   **/styles** - Kendo UI minified css styles 

### Installing and Getting Started with Kendo UI

Kendo UI is a pure JavaScript library, so installing and getting started is quick and easy:

1.  Download Kendo UI
2.  Copy the Kendo UI CSS and JavaScript resources to your project
3.  Configure your page to use Kendo UI scripts and skins:&nbsp;

     **Kendo UI Web**  
        <!--In the header of your page, paste the following for Kendo UI Web styles-->
    <link href="styles/kendo.common.min.css" rel="stylesheet" type="text/css" />
    <link href="styles/kendo.default.min.css" rel="stylesheet" type="text/css" />
    
    <!--Then paste the following for Kendo UI Web scripts-->
    <script src="js/jquery.min.js" type="text/javascript"></script>
    <script src="js/kendo.web.min.js" type="text/javascript"></script>
      **Kendo UI DataViz**  
        <!--In the header of your page, paste the following for Kendo UI DataViz style sheet -->
    <link href="styles/kendo.dataviz.min.css" rel="stylesheet" type="text/css" />
    
    <!--Then paste the following for Kendo UI DataViz scripts-->
    <script src="js/jquery.min.js" type="text/javascript"></script>
    <script src="js/kendo.dataviz.min.js" type="text/javascript"></script>
      **Kendo UI Mobile**  
        <!--In the header of your page, paste the following for Kendo UI Mobile styles-->
    <link href="styles/kendo.mobile.all.min.css" rel="stylesheet" type="text/css" />
    
    <!--Then paste the following for Kendo UI Mobile scripts-->
    <script src="js/jquery.min.js" type="text/javascript"></script>
    <script src="js/kendo.mobile.min.js" type="text/javascript"></script>
     4.  You are now ready to use Kendo UI. [Check the demos](http://demos.kendoui.com/) to see how quickly you can begin building
rich HTML5 applications. 

## Technical Requirements

Below are the system requirements for the Kendo UI Framework.&nbsp;
 <section class="twoColumns firstColumn"> 

#### Browser support
 <table class="devices-platforms stripes"> <tbody> <tr> <th class="browsers"> </th> <th class="browsers-windows">Windows</th> <th class="browsers-mac">Mac OS</th> <th class="browsers">Linux</th> </tr> <tr> <td><span class="ie"></span>Internet Explorer</td> <td>7.0 +</td> <td>-</td> <td>-</td> </tr> <tr> <td><span class="firefox"></span>Firefox</td> <td>[ESR](http://www.mozilla.org/en-US/firefox/organizations/faq/)</td> <td>[ESR](http://www.mozilla.org/en-US/firefox/organizations/faq/)</td> <td>[ESR](http://www.mozilla.org/en-US/firefox/organizations/faq/)</td> </tr> <tr> <td><span class="chrome"></span>Chrome</td> <td>Yes</td> <td>Yes</td> <td>Yes</td> </tr> <tr> <td><span class="opera"></span>Opera</td> <td>10.0 +</td> <td>10.0 +</td> <td>10.0 +</td> </tr> <tr> <td><span class="safari"></span>Safari</td> <td>4.0 +</td> <td>4.0 +</td> <td>-</td> </tr> </tbody> </table> 

***** Previous versions are supported with some limitations
 **NOTE: Browsers in BETA stage are not supported. Also&nbsp;note that Internet Explorer Quirksmode is not supported as it uses IE 5.5 rendering engine. Always specify [DOCTYPE](http://reference.sitepoint.com/html/doctypes) on your pages!
 **
 </section><section class="twoColumns"> 

#### Platform support
 <table class="devices-platforms stripes"> <tbody> <tr> <th class="platform"> </th> <th class="platform-version">&nbsp;&nbsp;Version</th> </tr> <tr> <td style="width: 100px;"><span class="windows"></span> Windows</td> <td>XP / Vista / 7 /Server 2003,2008 R1,R2

        32,64-bit editions</td> </tr> <tr> <td><span class="mac"></span> Mac OS</td> <td>OS X +</td> </tr> <tr> <td><span class="android"></span> Android</td> <td>2.0 +</td> </tr> <tr> <td><span class="ios"></span> iOS</td> <td>3.0 +</td> </tr> <tr> <td><span class="blackberry"></span>BlackBerry</td> <td>6.0+</td> </tr> <tr> <td><span class="webos"></span>WebOS</td> <td>2.2+</td> </tr> <!--<tr><td><span class="winphone"></span> Windows Phone</td><td>1.0 +</td></tr><tr><td><span class="palm"></span> Palm</td><td>9.0 +</td></tr><tr><td><span class="symbian"></span> Symbian</td><td>3.0 +</td></tr>--> </tbody> </table>
*Kendo UI Mobile currently supports iOS 3.0+, Android 2.0+ and BlackBerry touchscreen devices.

&nbsp;

Prerequisites:

*   JavaScript must be enabled on all browsers 

For best performance:

*   'Disable script debugging' in the browser's config options must be checked
*   Caching on Internet Explorer must be activated </section> <div class="clear"></div> 

&nbsp;
 [Send Feedback](mailto:documentation@kendoui.com?subject=Kendo%20UI%20Documentation%20Feedback&amp;body=Please%20add%20the%20Url%20of%20the%20corresponding%20help%20article.%20This%20will%20allow%20the%20appropriate%20team%20to%20handle%20your%20feedback%20accordingly.%0A%0AYour%20feedback%20is%20used%20to%20improve%20the%20documentation%20and%20the%20product.%20Your%20e-mail%20address%20will%20not%20be%20used%20for%20any%20other%20purpose%20and%20is%20disposed%20of%20after%20the%20issue%20you%20report%20is%20resolved.%20%20While%20working%20to%20resolve%20the%20issue%20that%20you%20report%2C%20you%20may%20be%20contacted%20via%20e-mail%20to%20get%20further%20details%20or%20clarification%20on%20the%20feedback%20you%20sent.%20After%20the%20issue%20you%20report%20has%20been%20addressed%2C%20you%20may%20receive%20an%20e-mail%20to%20let%20you%20know%20that%20your%20feedback%20has%20been%20addressed.)