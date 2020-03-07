---
title: Structure
layout: doc
permalink: /core/
---

FAIR-biomed is designed as a core application with a library of plugins.
 
The [github repository](https://www.github.com/fair-biomed/fair-biomed) has a small number of directories. 

 - `docs` holds a small number of files used in the repository README. Most of the documentation is maintained in a [separate repository](https://github.com/FAIR-biomed/fair-biomed.github.io).
 - `library` holds a collection of plugins, each of which interacts with one external data resource.  
  - `src` holds the source code for the core application.
 - `test` holds unit tests for the core application.
 
Other directories are created during installation and development.
 
 - `node_modules` holds third-party javascript/node packages. 
 - `dist` holds the 'compiled' version of the extension that can be loaded into a browser.   
 
Although all these components are necessary to build the extension, you can create a new plugin by working entirely within the `library` folder and without accessing the parts.
 
