zoomable-treemap-csv
====================

D3 zoomable treemap populated from a CSV file

Based on the initial zoomable treemap example from Mike Bostock. You can find the initial code here : http://mbostock.github.io/d3/talk/20111018/treemap.html.

The idea of this version of the zoomable treemap is :
- to populate the treeview from CSV data instead of JSON document.
- keep the configuration as much simple as possible (without editing the core page)

In practice the configuration is done by a simple JSON document "config.json". There are few parameters you can play with to read your data :
- document : this is the name of your CSV file. 
- separator : the character used to separate the rows inside the document. Most of the time you want to use a coma, but in some countries CSV files can use differents delimiters (for example ";"... yes it's no longer CSV).
- hierarchy : list of the columns used to group data.
- values : list of the columns that contains the values.
- label : name of the column that contain the text to display in each cell.
- tooltip (optional) : name of the colum that contain a tooltip that is showed when you hoover a cell.

Here is an example of configuration :
```
{
 "document" : "example.csv",
 "separator": ";",
 "hierarchy": [ "group1", "group2" ],
 "values":    [ "size", "occurences"],
 "label":     "title",
 "tooltip":   "tip"
}
```
FBranca/d3-zoomable-treemap-csv/blob/master/sampledata/baseball.csv
You can see a full example running [here](treemap.html) with its [configuration file](config.json) and the [csv file](sampledata/baseball.csv).
