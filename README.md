# scholarly-trend-explorer

Before execution, the required Apache Solr indexes need to be created and populated. 
Three indices are required: one for noun phrases, one for Wikipedia entities, and a third intermediate index (arxiv_metadata) which is used to populate the published date in the first 2 indices from Arxiv's metadata.
The Python indexing programs and the Solr configuration files are provided under Indexing/.

Execution:
```
python[3] phrases_or_entities_over_time.py 
```

On the web page, there is an input box with two sets of radio buttons. Another input box appears when the 'cluster' radio button is selected.
- Radio Button Set 1: Noun phrase visualization, Wikipedia entity visualization, cluster visualizations
- Radio Button Set 2: Time interval: chosen from 'monthly' or 'yearly'.

The graphs update automatically based on the values in the input box and the selected radio buttons. 

## Options
1. __Noun phrase visualization:__ Enter one or more noun phrases in the input box and select the time interval of
   your choice to generate a graph with Time on the x-axis and Percentage of papers which contain the noun phrase(s)
   on the y-axis.
2. __Entity mention visualization:__ Enter one or more Wikipedia entities in the input box and select the time interval of
   your choice to generate a graph with Time on the x-axis and Percentage of papers which contain the Wikipedia entites
   on the y-axis. Note that you can either enter the entire Wikipedia URL or just enter a noun phrase. If a noun phrase
   is entered, the system replaces spaces in the noun phrase with underscores and prefixes it with http://en.wikipedia.org/wiki/

3. __Cluster Visualization:__ If you click on the 'cluster' radio button, a dropdown box appears. 
   If there is nothing entered in the 1st input box while clicking on 'cluster' (and the dropdown is left blank), trends of all 50 clusters are shown.
   
   If you select a cluster from the dropdown, the trend of that cluster is displayed along with the words in that cluster.


4. __Cluster Visualization 2:__ Typing a noun phrase like 'machine learning' in the first input box plots the trend of the appropriate cluster
   to which the noun phrase belongs.


## Demo 
A demo of the system is available online at http://scholarsight.org/.


## Contact
The system has been designed and implemented by Michael Färber and Ashwath Sampath. Feel free to reach out to us in case of questions or suggestions:

[Michael Färber](https://sites.google.com/view/michaelfaerber), michael.faerber@cs&#46;uni-freiburg&#46;de
