---
title: Setup
layout: doc
permalink: /setup/
---

To create a development environment where you can adjust the code or create a new plugin, first download the [source code](https://github.com/FAIR-biomed/FAIR-biomed).  

If you would only like to experiment with the repo, you can just clone the source repository into a local directory. If you would like to develop new components and merge with the parent project, make a fork first and then clone the forked version.


## Install dependencies

After you have a local copy of the source code, the next steps are to install all dependencies and then building the application. 

Install all dependencies using the node package manager.

```bash
npm install
```

This step may take time as several dependencies are installed in a new folder `node_modules`. 


## Test

The next stage in the installation process is testing. Although testing is sometimes an optional step during an installation procedure, that is not the case for FAIR-biomed. The testing stage evaluates the types of plugins that are available and in working condition. Only properly functioning plugins are made available for the next build stage.

Run the entire test suite.

```
npm run test
```

This should display a positive message at the end.


## Build the extension

The build process prepares the core extension code as well as the plugins into a form that can be understood by a browser. The process bundles together javascript, html, and other files together.

Build the app. 

```
npm run build
```

This command creates a a directory `dist` and populates it with files. 

The default behavior for the build process is to prepare the extension for the Chrome browser. To specify the target browser, you can use one of the following commands.

```
BROWSER=chrome npm run build
BROWSER=firefox npm run build
```


## Load into the browser

After the build step, add the extension to your browser. 

In Chrome, find the customization menu (icon with vertical dots beside the navigation bar). Select `More tools` and then `Extensions`. A new tab should appear listing your existing extensions. Turn on `developer mode` (switch on top-right), then press the `Load unpacked` button. In the popup window, select the location of the `dist` folder. 

In Firefox, find the customization menu (icon with three bars beside the navigation bar). Select `Add ons`. A new tab should appear. Make sure `Extensions` is selected on the left-hand side. Find the heading `Manage your extensions`, press the configuration button (icon with a cog). ...



## Developing and testing
 
If you are aiming to develop new components, look into `package.json` to examine the steps to generate the core of the extension as well as the plugin library. 

