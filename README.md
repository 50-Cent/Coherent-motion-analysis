# CoherentMotionAnalysisToolbox

The 'Coherent Motion' tool of a noisy time-series data is based on a statistical trend detection procedure, Theil-Sen trend map. 
In this algorithm, a median trend is computed of an uniform or nonuniform time series. It is entirely a point-based operation; 
therefore no geological structural analysis is needed.

The 'Coherent Motion' tool takes a feature layer with point feature class as input and gives two separate output layers.

The first output layer exhibits the absolute value of linear trend of each point in the input layer. 
The trends are colored encoded in the symbology layer based on warning threshold and critical threshold.

The second output layer shows a set of polygons based on a group of points that are determined within a specified scale 
and that has absolute trend value more than warning threshold. This tool automatically save a shapefile for the polygon 
featureclass in the background. The polygons are colored based on another input symbology layer. As an example, a red polygon 
indicates that there exists at least one point that has an absolute trend value more than the critical threshold. The minimum 
number of points that are allowed to form a polygon within the scale is set as '3' within the script. 
