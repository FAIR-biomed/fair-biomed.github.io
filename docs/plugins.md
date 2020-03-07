---
title: Plugins
layout: doc
permalink: /plugins/
---


FAIR-biomed is powered by a library of plugins, each of which accesses data from one external data resources. Plugin definitions are located in subdirectories of `library`. For example, plugins accessing data from the [Wikimedia foundation](https://www.wikimedia.org) are located in `library/wikimedia`.


## Plugin files

Plugins are lightweight components that link between the core app and science APIs. In order to create this interaction, a canonical plugin consists of several files.

 - A javascript file implementing a specific set of fields and functions to establish an interaction between the core application and the external API. 

 - An image file with the logo of the external data resource.
 
 - A text file with a short description of the external data resource.
 
 - Another javascript (extension `js`) with unit tests for the primary plugin definition. 
 


## Module structure

The primary javascript file must have a `js` extension and hold a javascript module. The module must implement a specific set of fields (variables) and functions. 
 
**Static fields:**

 - `id` - string, a unique identifier for the plugin. This is never seen by the end user, but it is used by the core app.
 - `title` - string, a short heading of the plugin. 
 - `subtitle` - string, a short description. 
 - `tags` - array of strings, keywords associated with the plugin. 
 - `logo` - string, filename of a logo image file (svg, png, jpg).
 - `info` - string, filename of a text/html file containing a description of the data source
 - `endpoints` - array of URLs, access points for application programming interfaces (APIs) at the biomedical resources. 
 
**Functions:**

 - `claim(query)` determines whether the plugin is displayed in the list of suggestions for a particular query. Here, the input `query` is always a string. The function should return a number [0,1] signaling to what extent the plugin can provide useful information about the query. Higher numbers give the plugin a higher ranking in the results list.
 - `url(query, index)` should construct a URL for an API call for the given query string. An integer index can be used if plugins require multiple round-trips to the API.
 - `process(response, index)` should transform data obtained from an API call into a simple object that can be displayed within the extension's output window. An integer index can be used if plugins require multiple round-trips to the API.
 - `external(query)` should construct a url to a human-readable page holding more information pertaining to a query. 

Note that a plugin directory can contain more than one plugin definition file. However, each file can define only one plugin. 



## Testing

Testing is carried out at two levels. The first is programmatic testing via unit tests. The test procedure described on the [setup](../setup/) page runs tests for all plugins, but it is also possible to execute tests specific to one plugin using the `test-plugin` script.

```
npm run test-plugin library/wikimedia
```

This executes a small number of tests on each plugin in the provided directory. These automated tests check that the required fields and functions are defined and return reasonable values.

Additional, plugin-specific, tests can be included into the testing framework by adding test files into the plugin folders. These test files must be named as `test-[plugin-name].js`. 

The second level of testing focuses on getting the plugin to display proper information in the browser. For this, follow the [setup](../setup/) procedure. To build the extension with the entire plugin library:

```
npm run test
npm run build
```

To build the extension with only a specific plugin:

```
npm run test-plugin library/wikimedia
npm run build-lib library/wikimedia
```

The build script also performs some checks and signals development hints. After a successful library build, reload the extension in the browser, navigate to a relevant page (or refresh an existing tab), and check whether relevant queries provide the expected output.  


## Examples

Existing plugins in the library folder can be used as templates. The list here contains some plugins that contain certain specific design patterns.

 - `library/uniprot/uniprot.search.js`, [here](https://github.com/FAIR-biomed/FAIR-biomed/blob/master/library/uniprot/uniprot.search.js), displays information about genes or proteins from several organisms. This module has a rather minimal structure. Its `claim` function uses some rudimentary logic to check if a query is potentially a gene or protein.
 
 - `library/ncbi/gene/ncbi.gene.js`, [here](https://github.com/FAIR-biomed/FAIR-biomed/blob/master/library/ncbi/gene/ncbi.gene.js), displays brief summaries on gene function. This module uses a two-pass system in its `url` and `process` function. In a first pass, the module uses `url` to construct a search query to the NCBI API, and uses `process` to extract a gene identifier that matches the query. In the second pass, the `url` function constructs a different API query to fetch the gene description, and the `process` function arranges the response into a table.

 - `library/europepmc/`, [here](https://github.com/FAIR-biomed/FAIR-biomed/tree/master/library/europepmc), holds a plugin that displays publications related to any query. The plugin directory contains a file with unit tests specific to that plugin. In particular, this example shows how to use preset API responses within the unit tests. 

