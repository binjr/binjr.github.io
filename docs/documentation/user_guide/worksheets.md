# Worksheet pane

<style>
    video {
        width: 100%;
        height: auto;
        box-shadow: 0 0 .2rem rgba(0, 0, 0, .1), 0 .2rem .4rem rgba(0, 0, 0, .2);
    }
</style>

A “worksheet” is where you’ll be adding the time-series you want to visualize from the connected data sources.

There are several types of worksheets in _binjr_, that offers different visual representations depending on the data type of the series exposed by a data source.

The two main types of worksheets currently available are:

* [Charts worksheets](#charts-worksheets)
* [Logs worksheets](#logs-worksheets)

## Navigation

Regardless of their types, worksheets share a common way of navigating through the timeline.

### Selecting the time range

Use the time range picker to select the worksheet current time range. 

!!! Info "Note"
    Invoke the time range picker by clicking the "From... To..." label at the center of the navigation bar.
    
    ![](/assets/images/worksheet_time_range_picker.png)
    
Select the start and end dates for the time range using the calendar widget, or choose a preset time range (Last 24 Hours, 
Last 90 Days, Today, etc...)

!!! Example "Example"
    <video controls  muted src="/assets/videos/worksheet_timerange_picker.mp4" type="video/mp4"/></video>

### Navigation history

All changes to a worksheet's time line are automatically remembered by the application, and you can navigate that 
history using the "backward" and "forward" arrows to the left of the navigation bar.

!!! Example "Example"
    <video controls  muted src="/assets/videos/worksheet_navigation_history.mp4" type="video/mp4"/></video>

### Linking worksheets timelines

All charts in a worksheet share a single time line, but worksheets are independent from one another; changing the 
current time on a worksheet does not affect the other.

It is sometime useful to navigate multiple worksheets conjointly (especially if they are in 
[separate windows](#detaching-tabs)), however, in which case you can link two or more worksheets by clicking on the 
"chain" icon on a worksheet tab.

All changes to the selected time range in a worksheet will then by applied to all linked worksheets as well.

!!! Example "Example"
    <video controls  muted src="/assets/videos/worksheet_link_timelines.mp4" type="video/mp4"/></video>
    
!!! Tip
    You can link all the worksheets of a runtime instance of binjr, even the ones in separate windows.  
    It is also possible to link worksheets of different types (e.g. charts and logs)
    
    You cannot, however, link worksheets from different processes. 


## Edition

You can edit and change the following properties, common to all worksheets/

### Renaming a worksheet
You can change the name of a worksheet at any time by double-clicking on its tab.

!!! Example "Example"
    <video controls  muted src="/assets/videos/rename_worksheet.mp4" type="video/mp4"/></video>

### Detaching tabs

Drag the tab handle of a worksheet and drop it *outside of the worksheet area* (or out of the binjr window 
entirely) to move this worksheet into a new, independent window.

Drop a detached tab *inside the worksheet area* of the main window to reattach it.

!!! Example "Example"
    <video controls  muted src="/assets/videos/worksheet_detach_tabs.mp4" type="video/mp4"/></video>


### Context menu

All tab actions can also be access via a context menu, invoked by right-clicking on a tab handle, or via the "Worksheets"
entry in the menu bar.

!!! Example "Example"
    <video controls  muted src="/assets/videos/worksheet_context_menu.mp4" type="video/mp4"/></video>


### Expand/Reduce series view

A large portion of the application's window is used up by the controls needed to help users compose a custom view of 
the data efficiently; the source pane, chart properties panel and detailed series table list.

All this real-estate, however, becomes wasted once the view is set up and all you want is to navigate it or present it 
to an audience.

In that case you can expand the series view so that it takes up the totality of the application's window, 
save fot the menu bar, and a condensed legend is display beneath each chart.

You can switch between an expanded and reduce view of the series visualization area at any time, by pressing the icon on the 
navigation bar, or by pressing `Ctrl+M`.

!!! Example "Example"
    <video controls  muted src="/assets/videos/worsheet_switch_modes.mp4" type="video/mp4"/></video>
    
!!! Tip
    While you cannot add new series when the view is expanded, all the navigation features (time range 
    picker, zoom, navigation history) are still available.
