# User Guide
* [Landing screen](#landing-screen)
* [Adding a source](#adding-a-source)
* [Adding a Worksheet](#adding-a-worksheet)
* [Adding series to a worksheet](#adding-series-to-a-worksheet)
* [Working with time-series](#working-with-time-series)
* [Managing workspaces](#managing-workspaces)
* Settings
     
## Landing screen
The landing screen for binjr is composed of three main parts from left to right; the menu bar, which hosts icons for all of the main user interactions, the "source" pane where available time-series are displayed, and the "worksheet" pane where data representation and navigation takes place.

![](http://www.binjr.eu/assets/images/landing-page.png)

You can expand the menu bar by clicking the “menu” icon to reveal label for menu
items.

![](http://www.binjr.eu/assets/images/expand-menu.png)

Click the icon again to hide the label and collapse the menu bar.

## Adding a source

A “source” is a link to the data provider for the time-series you’ll be
manipulating with binjr.

To add a new source to a workspace, use the menu bar to navigate to
Sources&gt; New Source and select the type of source to add:

![](http://www.binjr.eu/assets/images/new-source.png)

Alternatively, if there are no sources in the current workspace yet, you
can click on the icon on the left pane:

![](http://www.binjr.eu/assets/images/new-source-2.png)

If one or more sources have already been added, you can add another one
by clicking on the “+” icon next to the last tab:

![](http://www.binjr.eu/assets/images/new-source-3.png)

### Adding a JRDS source

If you selected to add a JRDS instance as a source, the following dialog
will show:

![](http://www.binjr.eu/assets/images/new-source-4.png)

Fill in the desired URL, time zone and type of view filter to open the
source.

## Adding a worksheet

A “worksheet” is where you’ll be adding from various sources the
time-series you want to visualize.

It mainly contains a chart view where the time-series data will be
plotted and a table view listing the various series that were added to
the worksheet:

![](http://www.binjr.eu/assets/images/worksheet.png)

To add a worksheet to the current workspace, use the menu bar to
navigate to Worksheet and select New Worksheet (or press Ctrl+W):

![](http://www.binjr.eu/assets/images/new-worksheet.png)

Similarly to sources, clicking on the background chart icon on an empty
pane or on the “+” tab, will also invoke the new worksheet dialog.

![](http://www.binjr.eu/assets/images/new-worksheet-2.png)

When creating a new worksheet, you’ll be prompted to specify:
-   A name for the worksheet.
-   The type of chart it will host, to choose from:
    -   An area chart
    -   A stacked area chart
-   The label of the unit that the Y axis will represent
-   The unit prefix to use for Y axis value, to choose from:
    -   Metric: values on the Y axis will be divided by factors of 1000
        and use metric prefix, such as Kilo, Mega, Giga, etc…
    -   Binary: values on the Y axis will be divided by factors of 1024
        and use binary prefix, such as Kibi, Mebi, Gibi, etc…
-   The time zone for the time (e.g. X) axis
-   The initial time interval of the series

### Editing the name of an existing worksheet

Once a worksheet has been created, you can change its name at any time by double-clicking on its tab:

![](http://www.binjr.eu/assets/images/edit-worksheet-name.png)

## Adding series to a worksheet

Once one or more sources have been added, navigate to the indicator you want to add to a worksheet using the tree.
Right-click on the one you want to add and a context menu appears:

![](http://www.binjr.eu/assets/images/add-source-to-new-worksheet.png)

Note that in this case, the properties of the new worksheet are pre-populated with info retrieved from the source, if present:

![](http://www.binjr.eu/assets/images/new-worksheet-dialog.png)

You can also add additional series to an existing worksheet, by selecting "Add to current worksheet" in the context menu:

![](http://www.binjr.eu/assets/images/add-to-existing.png)

## Working with time-series

### Navigating the chart
#### Scaling the Y axis
#### Zooming the chart
#### History
### Time-series order and appearance
#### Selecting active series
#### Changing series order
#### Changing series color
### Taking snapshots

# Managing workspaces
