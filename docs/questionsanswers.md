---
title: Questions & answers
layout: doc
permalink: /questionsanswers/
---


## Using plugins

### Why are some databases included in FAIR-biomed, but not others? 

FAIR-biomed is built through a collaborative effort so its content
reflects what users' have found useful in the past. But the extension
has a modular architecture and can be extended to interact with any
database in the biomedical domain, as long as it provides an open 
application programming interface (API).

You can request for a database to be included, or volunteer to write 
a new plugin, by [raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).  


### How do I know what I can search for in any given database / plugin?

While some databases can perform searches based on arbitrary content, other databases require specific inputs such as identifiers or genomic coordinates. 

To see examples of the inputs that can be processed by any one plugin, first
try to run a query with any kind of input. Even if you don't see useful output,
the results pane will display a toolbar at the bottom. Click on the information
icon - the information panel should contain example queries.

Another way to see example queries is in the extension configuration page. 
To reach that, click on the extension icon on the browser toolbar (it is usually in the top-right corner). Click on the cog icon, and then explore information
associated with all the plugins.


### <a name="qa1"></a> A database has information about a topic; why doesn't the FAIR-biomed plugin display it? 
  
Some data portals hold multi-faceted information. For example, [Reactome](https://reactome.org/) can link gene symbols to proteins, sequences, pathways, and so on. Their data portal has a complete user interface to navigate these 
different facets. FAIR-biomed, in contrast, aims to display only a snippet
of the entire content. For Reactome, for example, the extension only lists 
pathways and omits all other information. This is due to the limited space 
available in the popup to display information. Hopefully, the link to the external data resource will facilitate access to other facets.


### A plugin stopped working - why?

FAIR-biomed plugins rely on application programming interfaces (APIs) 
provided by external databases. These external databases sometimes update their
server infrastructure and, if the modifications include changes to the APIs, 
FAIR-biomed plugins must also be updated.   

If you think a plugin has stopped working because of an API change, please
[raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).  


## Error messages

### What does 'The server reported no hits for this query' mean?

This message appears when a search is technically successful, but the 
external database has no information to display about the query. 

There can be several reasons for an empty search result. It is possible that, indeed, the database does not have relevant information. For example, search 'ABCABC' in [HGNC](www.genenames.org) reports this message because the search query is not a valid gene symbol. 

However, it is important to note that FAIR-biomed plugins usually query only one API endpoint (see a previous question '[A database has information about a topic; why doesn't FAIR-biomed display it?](#qa1)').
 

### What does 'Error processing server response' mean?

This message appears when an external resource provides data, but a FAIR-biomed
encounters an error in processing that data. This may occur if the external
database is temporarily malfunctioning. If the error persists, the error is probably a sign of a bug in a FAIR-biomed plugin. Please report it by [raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).


### I see another type of error message - what does that mean?

FAIR-biomed plugins process data provided by the external databases and prepare it for display. These plugins can choose to display any content, including 
custom error messages. Ideally, these should be informative. If not, please
[raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues). 

