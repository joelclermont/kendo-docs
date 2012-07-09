---
title: ThemeBuilder
slug: gs-themebuilder
tags: themebuilder, customization, css
publish: true
---

### What is the Kendo ThemeBuilder?

The Kendo ThemeBuilder is a tool that lets you modify Kendo themes so that they match the look and feel of your site or app.

### Using the ThemeBuilder on your own pages

Because the ThemeBuilder is a browser bookmarklet, using it on your own pages is as easy as clicking a button. Just drag the ThemeBuilder button to your bookmarks bar, and voila! You can now load the theming interface on every page that contains Kendo components.

### Using the output from the ThemeBuilder

Since the ThemeBuilder can output LESS or CSS text, you need to perform a few steps to use the newly created theme on your pages.

#### Using the CSS output

Just copy the CSS output to a .css file and include it in your page.

#### Using the LESS output

The LESS output of the ThemeBuilder depends on the template.less theme template that is distributed along with the Kendo UI source. Save the LESS output to a .less file alongside the template.less and refer to the [official LESS documentation](http://lesscss.org/#-client-side-usage) on the various ways you can process it.