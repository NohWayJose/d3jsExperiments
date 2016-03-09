# d3jsExperiments
Some data visualisation - particularly solar power generation
This code aims to do the following
1/ visualise power generation data that is recorded every ten minutes during daylight hours.
2/ Represent the data in a way that allows comparison between years
3/ At maximum zoom, see ten minute data resolution
4/ At minimum zoom (1 year), see data averaged for 1 day (not sure of the utility of this)
5/ At intermediate zooms use an appropriate granularity of data to allow it to remain responsive and yet representative
6/ Vary the Y-axis amplitude on-demand
7/ Oversample on the X-Axis, compared to the default for a selected zoom level (twice or four times oversample, for example)

I have used d3js to create a circular X-Axis graph with days, weeks & months on the X-Axis and kWh on the Y-Axis
(it's not a radar chart, it's a polar plot). Each year should be a different trace
