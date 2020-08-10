---
title: Questions & answers
layout: doc
permalink: /questionsanswers/
---


## Using plugins

### Why are some databases included in FAIR-biomed, but not others? 

FAIR-biomed is built through a collaborative effort so its content
reflects users' interests. 

But the extension has a modular architecture and can be extended to interact 
with any database in the biomedical domain, as long as it provides an open
application programming interface (API).

You can request for a database to be included, or volunteer to write 
a new plugin. Please [raise a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).  


### How do I know what I can search for in any given database / plugin?

While some databases can perform searches based on arbitrary content, other 
databases require specific inputs such as identifiers or genomic coordinates. 

To see examples of the inputs that can be processed by any one plugin, first
try to run a query with any kind of input. Even if you don't see useful output,
the results pane will display a toolbar at the bottom. Click on the information
icon - that should display a summary about the database and example queries.

Another way to see example queries is in the extension configuration page. 
Click on the extension icon on the browser toolbar (it is usually in the 
top-right corner). Click on the cog icon, and then explore information
associated with the plugins.


### <a name="qa1"></a> A database has information about a topic; why doesn't the FAIR-biomed plugin display it? 
  
Some data portals hold multi-faceted information. For example, [Reactome](https://reactome.org/) can link gene symbols to proteins, sequences, pathways, and so on. Their data portal has a complete user interface to navigate these 
different facets. FAIR-biomed, in contrast, aims to display only a snippet
of the entire content. For Reactome, for example, the extension only lists 
pathways and omits all other information. This is due to the limited space 
available in the popup. Hopefully, the link to the external data resource will 
facilitate access to other facets.


### The list of plugins suggested for my queries includes many that lead to empty results; why can't the list be pruned?

The list of plugins suggested for a particular query is produced by analyzing
the query text only, not based on downloaded data, so may indeed contain false
positives. The motivation behind this design choice is to minimize unnecessary
data requests.

It is worth noting that the extension records the number of times a plugin is 
used in practice. If a plugin is not used very often, it will appear lower in 
the ranking over time. Conversely, relevant plugins will appear at the top and 
should provide non-empty results for the type of queries that have been 
performed previously.


### A plugin stopped working - why?

FAIR-biomed plugins rely on application programming interfaces (APIs) 
provided by external databases. These databases sometimes update their
server infrastructure and, if the modifications change APIs, 
FAIR-biomed plugins must also be updated.   

If you think a plugin has stopped working because of an API change, please
[raise a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).  


## Messages

### What does '<span class="question">The database reported no hits for this query</span>' mean?

This message appears when a search is technically successful, but the 
external database has no information to display about the query. 

An empty search result may indicate that a database does not have relevant 
information. For example, this message appears when searching for 'ABCABC' in [HGNC](www.genenames.org) because 'ABCABC' is not a gene symbol. 

However, it is important to note that FAIR-biomed plugins usually query only 
one API endpoint (see ['A database has information about a topic; why doesn't FAIR-biomed display it?'](#qa1)). Thus, it is possible that
the database does not have information *of the type usually displayed by the 
plugin*, but a full query on the data portal may nonetheless provide useful
information.
 

### What does '<span class="question">Error processing server response</span>' mean?

This message appears when an external database provides data, but a FAIR-biomed
plugin encounters an error while processing that data. This may occur if the 
database is temporarily malfunctioning and sends ill-formatted data. 
If the error persists, then the error is probably a sign of a bug in a 
FAIR-biomed plugin. Please report it by [raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues).


### What does '<span class="question">Error, or server not available</span>' mean?

This means that FAIR-biomed could not interact with an external database and
could not send or receive data. A common cause for this error is a faulty 
internet connection - please check your network and try again. This error can 
also appear if an external database is down.


### What does '<span class="question">Server timed out</span>' mean?

This means that FAIR-biomed was able to interact with an external database, but 
the server did not send any data in response to a query. This may occur if the
network or external database is experiencing heavy load. Usually, this 
error should disappear when conditions return to normal.


### I see another type of error message - what does that mean?

FAIR-biomed plugins process data provided by external databases and prepare the
 data for display. Each plugin operates independently and processes data in its own way, and can generate custom messages. Ideally, these should be 
 informative. If not, please help improve the plugins by 
[raising a ticket on the github repository](https://github.com/fair-biomed/fair-biomed/issues). 

