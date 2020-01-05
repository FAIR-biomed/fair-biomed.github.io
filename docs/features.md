---
title: Features
layout: doc
permalink: /features/
---


## Triggers

There are two ways to trigger the FAIR-biomed popup.

- Select some text on a web page, then press `Ctrl+Shift+Z`.
- Select some text, use the mouse to right-click, and then select `FAIR-biomed search` from the context menu.

Both these methods trigger the FAIR-biomed popup, which appears with the selected text in its search box.

It is also possible to trigger the popup without first selecting any text. In this case, the popup appears empty. You can type into the search box to see available plugins.


## Toolbar

Whenever the extension displays a search result, a toolbar appears at the bottom of the popup box.  

<p align="center">
<img src="../images/toolbar.png" height="44">
</p>

Icons in the toolbar are buttons that provide additional information pertaining to the result.

<div class="features-img"><img src="../images/fa/table-solid.svg"></div> The default view is always the "table" view. This displays data provided by the online resource in response to a query. It is important to emphasize that the data displayed in this view is typically a small subset of the entire data available at the source.

<div class="features-img"><img src="../images/fa/info.svg"></div> The second button displays a static summary about the resource itself. Information in this view is meant to credit the source of data. Many plugins also provide example queries. 

<div class="features-img"><img src="../images/fa/code.svg"></div> The code button display the raw API call used to fetch information from the data resource. This URL can be copy-pasted into a browser window and the result will be the full output.

<div class="features-img"><img src="../images/fa/external-link-alt.svg"></div> The final button is a link to an external web page. Clicking this buttons opens a new browser tab, which loads a page from a data portal with more information on the query.


## Minimizing

Each popup has a small toolbar in its top-right corner.

<p align="center">
<img src="../images/min_close.png" height="30">
</p>

The "close" button makes the popup disappear. After this action, the popup is completely removed from the web page. 

The "minimize" button also makes the popup disappear, but keeps a version hidden in the background. You can click on a "syringe" next to originally highlighted text to make it visible again. This feature makes it possible to see results again without resending a query. The information also remains embedded inside the web page if the entire page is saved, and re-opened in a new browser session.


