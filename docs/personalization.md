---
title: Personalization
layout: doc
permalink: /personalization/
---


## Options

The extension has a dedicated page where you can tune several options, including which data sources you would like to use. 

 - Find the FAIR-biomed icon on the browser toolbar (it's usually in the top-right). Click on that icon and a small popup will appear.
 
<p align="center">
<img src="../images/options_popup.png" width="400">
</p>
 
 - Click on the <i class="fas fa-cogs"></i> icon. You will see a new tab the options page.

The bulk of the options page consists of a list of all the plugins. One of these is the IMPC plugin.

<p align="center">
<img src="../images/options_impc.png" width="100%">
</p>

 - Clicking on any of the items reveals/hides addition information about the plugin. This information typically describes the data resource that powers the plugin, and a few example queries.
 
 - Clicking on the slider turns a plugin on and off. When a plugin is off, it never appears in the list of suggestions. When a plugin is on, it can appear in the list of suggestions, but only when the plugin detects that query is appropriate. Thus, for example, a plugin that is designed to provide data on a genomic position will appear as a suggestion when the query is vaguely similar to a description of a chromosome and position, not a gene symbol.
 
 - Clicking the star symbol next to the slider marks the plugin as a "favorite". This status is displayed in the list of suggestions, but does not otherwise affect the presentation of the suggestions.


## Local URLs

The extension is active on all pages that you accesss via urls starting with 'http' or 'https'. By default - for security reasons - the extension is not active when viewing pages hosted on a local computer, i.e. files from a local disk. 

To use the extension with local URLs, you must enable this functionality manually. In chrome:
 
 - Select `More tools > Extensions` from the chrome menus; a new tab should appear listing all your installed extensions
 - Find `FAIR-biomed` and click `Details`; the view should change and display information about the extension
 - Scroll down to turn the switch labeled `Allow access to file URLs`.

