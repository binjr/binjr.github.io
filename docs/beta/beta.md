# binjr v3 beta announcement

Version 3 for binjr is getting ready for release :tada:

This is a major version change, justified by some fairly notable - and breaking - changes in both the plugin API
and the serialization format.

So we decided to first run a beta phase and gather feedback from the community, to make sure we're on the right track!

## What's new?

These breaking changes were necessary to accommodate a new core feature; the ability to visualize 
time series not only as charts of numeric values, but any other type of visualization for any data type.

The first use of this new ability is the addition of a data source adapter for log files. Log files, produced 
by applications to trace their lifecycle at runtime, typically contain timestamps for each event they contain; so we can
 think of them as time series, but with data points being textual information instead of numerical values.
 
In practical terms, this means that a lot of the features built into binjr to compose and navigate time series 
visualizations can be applied to log files with great benefits.  
For instance, in the same way binjr lets you mix series from different sources on the same chart, it allows for viewing 
events from different files on the same page, with all events being sorted based on their timestamp.  
Furthermore, binjr already lets you synchronize the time line for two or more separate tabs holding charts; you can 
now also link a log event tab in the same way. This means that the view for the logged event will be automatically 
refined as you zoom in or out on a linked chart (and vice versa).

## How does it work?

Behind the scene, binjr uses [Apache Lucene](https://lucene.apache.org/) to index data from log files; which allows to
efficiently sort, filter and search the
meaning users can use its powerful query language to hack through vast quantities logged events,

This also allows binjr to open log files of any size; unlike most text editors which will fail to load multi 
gigabytes-sized files as they try to fit it all in memory, binjr will happily index those and present a paginated view 
to guarantee memory usage remains reasonable, while the backing index ensures navigating and searching is lighting 
fast.

With these new abilities, the goal is for binjr to become the missing link between text editors and command line tools
traditionally used to analyse monitoring data locally and full-blown log analytics platforms (e.g. Elastic/Logstash/Kibana 
stack) that centralizes logs for entire organizations.    
It provides many of the same powerful visualization and search features while still remaining a totally 
local solution (the data never needs to be pushed to the cloud - or anywhere else for that matter), and requiring no 
setup nor maintenance to speak of.


## Tell us what you think!

Please give it a try and let us know what you think; what's good and what's not? What's missing? What's broken? 
What could be improved?

You can download the latest beta version from the project's [github release page](https:/github.com/binjr/binjr/releases)
and share your thoughts in the [dedicated discussion thread](https://github.com/binjr/binjr/discussions/107).   

You'll find the (Work-In-Progress) documentation for the new features [here](Using-binjr-to-view-logs.md).

If you run into a bug, please open an issue [here](https://github.com/binjr/binjr/issues).

Thanks!

