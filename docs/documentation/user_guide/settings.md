# Settings

<style>
    video {
        width: 100%;
        height: auto;
        box-shadow: 0 0 .2rem rgba(0, 0, 0, .1), 0 .2rem .4rem rgba(0, 0, 0, .2);
    }
</style>

You can access the "Settings" panel from the menu bar.

!!! Example "Example"
    <video controls  muted src="/assets/videos/settings_menu.mp4" type="video/mp4"/></video>
 
## Appearance & Behavior
### Theme

You can select binjr's user interface theme from this list. 

!!! Example "Example"
    <video controls  muted src="/assets/videos/settings_ui_theme.mp4" type="video/mp4"/></video>
    
**Default**: `Light`

### Span crosshair over all charts

Check this option if you want the vertical crosshair to span over all stacked charts on a worksheet. 

Uncheck it if you prefer it to only show over the focused chart.

!!! Example "Example"
    <video controls  muted src="/assets/videos/settings_span_crosshair.mp4" type="video/mp4"/></video>
    
!!! Info "Note"
    The timeline (X axis) for all charts in a worksheet are always aligned, regardless of this option.
    
**Default**: `Checked` 

### Reopen workspace

Check this option if you want the last opened workspace to be reloaded next time the application if started. 

Uncheck it if you prefer the application starts with a blank workspace.

**Default**: `Unchecked`

### Discard notification timer

The amount of time notifications popup should hover before being automatically dismissed.

**Default**: `10 Seconds`

### Snapshot output scale

The output scale factor to apply to snapshots.

**Default**: `Auto (Same as screen)`

## Charts
### Default color palette

Select the default color palette to use for series whose sources do not specify it.

**Default**: `Vibrant`

### Show outline on area charts

Check this option if you want newly created area charts to display a brighter coloured outline for each series.

**Default**: `Checked`

### Default area charts opacity

The default opacity value to apply to series on area charts.

**Default**: `30%`

### Show outline on stacked charts

Check this option if you want newly created stacked area charts to display a brighter coloured outline for each series.

**Default**: `Unchecked`

### Default stacked charts opacity

The default opacity value to apply to series on stacked area charts

**Default**: `70%`

### Enable sample reduction

**Default**: `Checked`

Check this option to enable sample reduction.

Sample reduction limits the number of samples to plot to improve chart rendering performances, using advanced 
algorithms[^1] to keep the best approximation of the original data.

[^1]: See https://github.com/sveinn-steinarsson/flot-downsample/ for more info on the down-sampling algorithms used by binjr.

!!! Warning "Note"
    It is highly recommended to always enable sample reduction, otherwise chart rendering performances might be 
    seriously affected.  
    
### Maximum number of samples

The maximum number of samples per time series to keep when sample reduction is enabled.

**Default**: `1500`

## Logs
### Default color palette

Select the default color palette to use for log files.

**Default**: `Vibrant`
 
## Data Adapters
### List of installed data adapters

This list shows all currently available data adapters.

You can enable or disable a data adapter using the check box next to its name in the list. 

A disabled data adapter no longer appears in the `New Source...` menu. Please note, however, that previously opened 
sources tab using this adapter will not be closed and data will still be fetched from it.

### Load from external folder

Check this option if you want to be load plugins from a specific location, in addition to those loaded from the classpath.

If checked, enter the location to load plugins from in the field beneath it.

!!! Info "Note"
    Plugins in the `/plugins` folder in a binjr installation are always loaded by the application, regardless of these 
    settings. 

**Default**: `Unchecked`

## Manage Settings
### Restore to default

Reset all settings to their default values.

### Export settings

Export the current values of all settings to a `.xml` file.

### Import settings

Import settings from a previously saved `.xml` file.

!!! Warning 
    This will overwrite the current values of all settings.
    
### Clear history

Clear all user history, such as most recently used workspaces, urls, files, saved folders, etc...

## Updates
### Check for updates on start-up

Check this option if you would like binjr to automatically check if an update available on start-up.

**Default**: `Checked`

### Check for updates

Click on the button if you would like to check for updates now.
