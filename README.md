# d3jsExperiments

Some time based data visualisation - particularly anually repetitive data, such as solar power generation

This sample code aims to do the following

1/ visualise power generation data that is recorded every ten minutes during daylight hours.

2/ Represent the data in a way that allows comparison between years

3/ At maximum zoom, see ten minute data resolution

4/ At minimum zoom (1 year), see data averaged for 1 day

5/ At intermediate zooms use an appropriate granularity of data to allow it to remain responsive and yet representative.

5b/ For the range shown there are cases where it might be worth seeing average, min, max & standard deviation (on demand) but exagerating the amplitude is likely to be necessary too. (see 6/)

6/ Vary the Y-axis amplitude on-demand (on my prototype this is an expandable dot in the centre of the graph - not yet functional)

7/ Explore oversampling on the X-Axis, compared to the default for a selected zoom level (twice or four times oversample, for example) - not sure what utility this might offer

8/ The graph is meant to be driven from a Maria (MySQL) DB which contains a datapoint for every ten minutes of daylight for the last four years. I wonder how I can query data from it quickly. Do stored procedures allow the dynamic creation & update of temporary tables, to cache data at different granularities, a bit like RRD Tool? ALternatively, should I use Maria to store the complete canonical data and populate RRDTool as the visualisation data source?

9/ A range slider could be used to zoom between a horizontal linear(ish) X-Axis, with a range of one hour - six (6x10minute) data points and a year (365x1day) data points. Preview of the range slider: http://htmlpreview.github.io/?https://github.com/NohWayJose/d3jsExperiments/blob/master/scopeWidget00.01.html

10/ I have used d3js to create a circular X-Axis graph with days, weeks & months on the X-Axis and kWh on the Y-Axis
(it's not a radar chart, it's a polar plot). Each year should be a different trace. Preview of the dataless chart: http://htmlpreview.github.io/?https://github.com/NohWayJose/d3jsExperiments/blob/master/SolarPower-v00.01.html
