# Using binjr to view logs

<style>
    video {
        width: 100%;
        height: auto;
        box-shadow: 0 0 .2rem rgba(0, 0, 0, .1), 0 .2rem .4rem rgba(0, 0, 0, .2);
    }
</style>

## Adding a log source

To add logs to a workspace, use the menu bar to navigate to
`Sources > New Source > Logs` 

Use the dialog box to select the path from which you want to load the log files, and the profile used to parse them.

!!! Example "Example"
    <video controls  muted src="/assets/beta/add_log_source.mp4" type="video/mp4"/></video>

!!! Tip
    binjr can load logs contained in zip archives directly, without the need to decompress them first. Just select a zip
    file instead of a folder in the `path` field.

A parsing profile is collection of settings that indicates how 

### Parsing profile editor


## Navigating the log view

### Use the severity facet

### Search bar

#### Query Syntax

Search for word "foo":  
`foo`

Search for word "foo" OR for word "bar":  
`foo bar` or `foo OR bar`

Search for phrase "foo bar":  
`"foo bar"`

Search for phrase "foo bar" *and* the phrase "quick fox":  
`"foo bar" AND "quick fox"` or `"foo bar" +"quick fox"`

Search for either the phrase "foo bar" AND the phrase "quick fox", or the phrase "hello world":  
`("foo bar" AND "quick fox")` OR `"hello world"`

Search for word "foo" and not "bar": (Note: The NOT operator cannot be used with just one term)  
`foo NOT bar` or `foo -bar`

Search for everything not containing "foo bar":  
`*:* NOT "foo bar""` or `*:* -"foo bar"`

Search for any word that starts with "foo":  
`foo*`

Search for any word that starts with "foo" and ends with bar:  
`foo*bar`

Search for a term similar in spelling to "foobar" (e.g. "fuzzy search"):  
`foobar~`

Search for "foo bar" within 4 words from each other:  
`"foo bar"~4` 
     







