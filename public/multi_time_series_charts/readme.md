###Shows How we can roll our own charting component with d3 for very specific needs. 
Here some utility libraries are used like 'underscore' for data transform, query and 'moment' for datetime operations.

Here the requirement is to compare time series continuous analogue values along with some digital inputs which are coming from different channels with irregular time intervals. Data are assumed to be coming as streams and hence the json format contains DateTime and value property.

Data formats:

 * Analougue: multi series (i.e. Acceleration data with three series X,Y,Z. See 'accelData' in sample_data.js)
 * Digital: grouped by Channel field (see diData in sample_data.js)
    

Look at the data format and how they are bound with d3 for our specific purpose.
	        
* Demonstrates how we can use d3's brush for zoom control over the shared x-axis without wasting space for a separate small chart for just zooming which most of chart component provides.
* Shows dynamic height adjustment as we add/remove new charts
* Shows how we can move charts up/down with smooth transitions with d3. This is one specific requirement that most chart components don't provide.

Thinkin of features..

* Realtime data update
* Horizon graph as render option for analogue data
* Resize based on window size
* Matching series colors - line color with legend value (or put colored marker)
* up/down button on each chart top-right corner to re-arrange the stack of charts for easy compare

Please comment in gist for suggestions/improvements et al.