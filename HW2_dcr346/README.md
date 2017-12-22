# PUI2017_dcr346/HW2_dcr346 - README.md

## Assignment 1+2
- request API Key, and set an env var to it
- parse json file to find appropriate fields
- Assignment 2: check the output within csv file 

## Assignment 3
- read in open data file using pandas
- make sure to select data with at least two numerical columns
- create simple scatter plot

## Extra credit
- read in open data file using pandas
- make sure to select data with at least one temporal value and one numerical value
- plot y variable dependant upon time


## Workflow and Collaboration:
The code was first writen in Jupyter notebook. After running it in notebook I copied it to emacs and changed the url to suit a py script with the env variables and sys.argv[] >> the methode was understandable to me. 

I worked with several students, primarily with Prince and Sarah: Learned from Sarah about the Json formatter for Google Chrome which made everything much more clear; Prince help me to better understand the difference between indexing a list and range(len(list)); Over the weekend we overviewed and finalized our scripts. I felt pretty good with navigating through the Json data structure.

For assignment 3+extra credit, before DF was all set I refered my Ipython notebook to a link from NYC Open Data website.
Sarah and I worked together on the third assignment. Rebecca then showed me how to access Urban Profiler from CUSP's Data Hub. For the extra credit, Unisse (and Google) helped me to figure out how to convert the str dates to date-time format.

## Notes:
My selected data in the extra credit assignment included a very large list of dates that didn't plotted properly (super-densed text); I reduced the number of plotted bars by assigning steps of 5 to the df2 values:

```
df2[::5].plot(kind="bar",x='Date', y='Block', rot=45, color="#D7F08F", figsize=(35,10), fontsize=15)
```
