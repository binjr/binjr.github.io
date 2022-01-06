# Supported data sources

***binjr*** can consume time series data provided by the following data sources:


|Name   | Description | Built-in[^1]          | Source type  |
|-------|-------------|-----------------------|--------------|
| [JRDS](https://github.com/fbacchella/jrds)      | A performance monitoring application written in Java. | :material-check:    | Remote |
| [Netdata](https://www.netdata.cloud)   | Distributed, real-time performance and health monitoring for systems and applications. | :material-check:    | Remote |
| RRD Files | Round-Robin Database files produced by [RRDtool](https://oss.oetiker.ch/rrdtool/) and [RRD4J](https://github.com/rrd4j/rrd4j). | :material-check:    | Local files | 
| CSV Files | Comma Separated Values files. | :material-check: | Local files | 
| Log Files | Text based, semi-structured log files. | :material-check:    | Local files | 
|[Demo Adapter](https://github.com/binjr/binjr-adapter-demo) |A plugin for binjr that provides data sources for demonstration purposes.|                       |Local files |


[^1]: Support for data sources not marked as *'Built-in'* requires additional plugins.