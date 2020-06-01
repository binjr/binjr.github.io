# What is binjr?

***binjr*** is a time series browser; it renders time series data produced by other applications as 
dynamically editable charts and provides advanced features to navigate the data smoothly and efficiently 
(drag & drop, zoom, history, detachable tabs, advanced time-range picker).
 
It is a standalone client application, that runs independently of the applications that produce the data; there are
no application server or server side components dedicated to ***binjr*** that needs to be installed on the source.   
Like a generic SQL browser only requires a driver to connect and retrieve data from a given DBMS, ***binjr*** 
only needs one specifically written piece of code - here called a data adapter - to enable the dialog with a specific 
source of time series data.

***binjr*** was originally designed - and it still mostly used - to browse performance metrics collected from computers 
and software components, but it was built as a forensic analysis tool, to investigate performance issues or applications
crashes, rather than as a typical monitoring application.   

Because of that, the user experience is more reminiscent of using a profiling application than a dashboard-oriented
monitoring platform; it revolves around enabling the user to compose a custom view by using any of the time-series 
exposed by the source, simply by dragging and dropping them on the view.  
That view then constantly evolves, as the user adds or removes series, from different sources, while navigating through 
it by changing the time range, the type of chart visualization and smaller aspects such as the colour or 
transparency for each individual series.  
The user can then save the current state of the session at any time to a file, in order to reopen it later or to share it 
with someone else.

# ...and what it isn't
* _binjr_ is **not** a system performance collector, nor a collector of anything else for that matter. What it provides is
   efficient navigation and pretty presentation for time series collected elsewhere. 
* _binjr_ is **not** a cloud solution. It's not even a server based solution; it's entirely a client application, 
  albeit one that can get its data from remote servers. Think of it as a browser, only just for time series. 
* _binjr_ is **not** a live system monitoring dashboard. While you can use it to connect to live sources, its feature set is
  not geared toward that particular task, and there are better tools for that out there. Instead, it aims to be an 
  investigation tool, for when you don't necessarily know what you're looking for beforehand and you'll want to build 
  and change the view of the data as you navigate through it rather than be constrained by pre-determined dashboards. 
 