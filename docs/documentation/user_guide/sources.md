# Source pane

<style>
    video {
        width: 100%;
        height: auto;
        box-shadow: 0 0 .2rem rgba(0, 0, 0, .1), 0 .2rem .4rem rgba(0, 0, 0, .2);
    }
</style>

A “source” is a link to the data provider for the time-series you’ll be manipulating with binjr, and the source pane 
shows the sources currently connected. 

!!! Tip
    You can toggle the visibility of the source pane using the "Show/Hide Source Pane" in the menu bar or by pressing 
    `Ctrl+L`

## Adding a source tab

To add a new source to a workspace, use the menu bar to navigate to
Sources &gt; New Source and select the type of source to add.

!!! Example "Example"
    <video controls muted src="/assets/videos/add_source_menu.mp4" type="video/mp4"/></video>

Alternatively, if there are no sources in the current workspace yet, you
can click on the icon on the left pane.

!!! Example "Example"
    <video controls  muted src="/assets/videos/add_source_icon.mp4" type="video/mp4"/></video>

you can add any number of sources, of any supported type to a single workspace.

!!! Example "Example"
    <video controls  muted src="/assets/videos/add_many_sources.mp4" type="video/mp4"/></video>


## Editing a source tab

Once you've successfully connected to a data source, all of its available time series are displayed in a tree view, 
with a hierarchy depending on the type of source.

![tree](/assets/images/source_tree_view.png)


Use the "filter" icon to filter out the series whose path matches the entered text.

!!! Example "Example"
    <video controls  muted src="/assets/videos/filter_tree_source.mp4" type="video/mp4"/></video>

Use the "cog" icon to change the name of of given source tab.

!!! Example "Example"
    <video controls  muted src="/assets/videos/rename_source.mp4" type="video/mp4"/></video>
    
    
    
## Built-in sources parameters    

### JRDS 

| Name | Description | Default|
|------|-------------|--------|
|**Address**  |The URL for the JRDS instance you want ot connect to. | |
|**Timezone**  | The time zone of the target JRDS instance| The host's current time zone. |
|**Sorted by**  | This parameter dictates the organization of the series tree view: <ul><li>`All Hosts`: Returns a tree sorted by hosts</li><li>`Host <host>`: Returns a view of for specified host only</li><li>`All Services`: Returns a tree sorted by services</li><li>`All Views`: Returns a tree sorted by views</li><li>`All Filters`: Returns a tree sorted by filters</li><li>`Filter <filter>`: Returns a view for the specified filter only</li><li>`All Tags`: Returns a tree sorted by tags</li><li>`Tag <tag>`: Returns a view for the specified tag only</li></ul>  | `All Hosts` |

### Netdata

| Name | Description | Default|
|------|-------------|--------|
|**Address**  |The URL for the Netdata instance you want ot connect to. | |

### CSV 

| Name | Description | Default|
|------|-------------|--------|
|**Path**  |The path to the CSV file you want to add to the source tab. | |
|**Timezone**  | The time zone corresponding to the capture timestamps in the CSV file. | The host's current time zone. |
|**Date Format**  | The pattern used to parse the timestamps. The syntax is that of Java's DatetimeFormatter: https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/time/format/DateTimeFormatter.html  |  `yyyy-MM-dd HH:mm:ss`   |
|**Encoding**  |    The encoding used in the CSV file      |  `utf-8`    |
|**Separator**  |  The character used as a column separator in the CSV file. | `,` |

!!! Warning "Note"
    The time stamps must be located in the **first** column of the CSV file. 

### RRD 

| Name | Description | Default|
|------|-------------|--------|
|**Path**  |The path to the RRD file(s) you want to add to the source tab. | |

!!! Tip
    You can add more than one RRD file to a single source tab.
    
    
### Log Files 

| Name | Description | Default|
|------|-------------|--------|
|**Path**  |The path to the CSV file you want to add to the source tab. | |
|**Timezone**  | The time zone corresponding to the capture timestamps in the log files. | The host's current time zone. |
|**Extensions**  | |`*.log`, `*.txt`| 
|**Parsing**  | The set of regular expressions that will be used to parse the log files into structured events. | `[Built-in] ISO-like timestamps`

!!! Tip
    Users can edit the existing sets of parsing rules and create their own via the [log parsing profiles editor](editing_parsing_profiles.md).

