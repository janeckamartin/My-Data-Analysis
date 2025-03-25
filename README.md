1. ENVIRONMENT CONFIGURATION

Start working on the project by creating a new notebook in Google Colab. Name it: covid_19_tracker.
Install (if necessary) and import the appropriate libraries (use aliases):
seaborn
pandas
matplotlib.pyplot (e.g. to control the size of seaborn plots)
plotly (including plotly express)
dash - modules that allow you to build a dashboard, such as dash_core_components or a module that allows you to insert HTML elements
threading - a library used to run multithreaded applications
output from google.colab - the module needed to display a chart

2. IMPORTING DATA

Send the*.csv with data downloaded from the project resources to the runtime environment.
Using the pandas library, create a data frame from a file uploaded to the execution environment.
Check the completeness of the data in the columns of the created data frame.

3. FIRST VIZUALIZATION

Using your data frame and the seaborn library, create a ranking that shows 10 countries with the largest populations in the set. Which country among the selected 10 has the largest population and which has the smallest one?
Adjust the visualization appearance:
Make the chart more readable by increasing the size of the figure.
Use the whitegrid style.
X-axis labels should be rotated so that they do not overlap. Hint: use the .set_xticklabels() method.

4. POPULATION VS. LIFE EXPECTANCY

Using your data frame and the plotly library, create a visualization that shows the relationship between population and life expectancy in a country. Do people live longer in countries that have larger populations?
Adjust the visualization appearance:
Set the X axis to use the logarithmic scale.
Set the color of the marker according to the continent where the country is located. Use a different color palette than the default one. You can use the palettes defined in Plotly or define your own palette as a list of colors.
Set an appropriate title for the chart.

5. NUMBER OF DIANOSED CASES

Using your data frame and the plotly library, create a visualization that shows how the number of new COVID-19 cases is distributed over time. Compare two countries of your choice.
Adjust the visualization appearance:
Make the color of the markers (markers = columns, lines, points - depending on which type of chart you apply to the defined problem) depend on the country where the number of cases was recorded.
Use a different color palette than the default one. You can use the palettes defined in Plotly or define your own palette as a list of colors.
Set an appropriate title for the chart.

6. COVID-19 MAP

Using your data frame and the plotly library, create a visualization that shows on a world map how many disease cases were reported in each country throughout the pandemic.
Adjust the visualization appearance:
Make the color of the markers dependent on the continents. Hint: Remember the best practices we discussed during prework and the first day of the course.
Make the size of the marker dependent on the ratio of cases to population in the country.
Set the initial zoom so that when the chart is generated, it is possible to see the entire world map.
Adjust the maximum size of the marker so that the chart is readable.
Adjust the tooltip so that when you hover over the marker, it shows the name of the country and information about the number of cases in that country.
Set the Mapbox dark style. *Hint: Mapbox was mentioned during the second day.
Set an appropriate title for the chart.

7. DASHBOARD 1

Using the plotly and dash libraries, create a dashboard consisting of two visualizations:

a line chart that shows the cumulative number of COVID-19 cases over time
a line chart that shows the cumulative number of COVID-19 deaths over time
We covered the topic of plotly on the first day of the course, and talked about dash during the third and fourth days.

The dashboard should consist of:
title that depends on the value of the filter (e.g. Cumulative number of positive cases in {country})
title (label) of the filter
filter by country, i.e. the user should be able to see charts only for the selected country
two visualizations placed side-by-side (in one line)
To run the dash application in Google Colab, use the solution presented in the course, based on the threading and google.colab libraries. Use the function that displays the application in a new browser tab.
*Hint: in case the application does not want to load, reset the runtime environment and restart all cells with code.

8. DASHBOARD 2

Using the plotly and dash library, create a dashboard consisting of one visualization:
map using the dark style from Mapbox, showing the markers of countries from the selected continent; with maker size depending on the value of the selected metric. For example, the user will be able to select the continent Europe and the measure: Total cases, resulting in markers (circles) appearing on the map in Europe. The larger the marker, the more cases in the country.
We covered the topic of plotly on the first day of the course, and we talked about dash during the third and fourth days. You will find the necessary information about Mapbox in the Mapbox API module at the end of the second day.

For calculations, use the data from the last day in the provided dataset.
The dashboard should consist of:
title that changes depending on the value of the filters according to the pattern: COVID-19 - {metric} in {continent}.
two filters:
filter to select the continent
filter to select a metric (total number of positive cases, total number of deaths, total number of tests, total number of vaccinations, total number of vaccinated people)
titles (labels) of filters
visualizations from the first point
When you hover over a marker, the name of the country appears in addition to the coordinates and metrics.
To run the dash application in Google Colab, use the solution presented in the course, based on the threading and google.colab libraries. Use the function that displays the application in a new browser tab.

9. DASHBOARD 3

Using the plotly and dash libraries, create a dashboard consisting of two visualizations:

column chart that shows the largest values of the total number of vaccinations for n selected countries (e.g., when n = 5 the chart shows the 5 countries with the most cases of disease, in descending order)
column chart that shows the largest values of the ratio of the total number of vaccinations to the population of a country, for n selected countries
We covered the topic of plotly on the first day of the course, and talked about dash during the third and fourth days.

For calculations, use the data from the last day in the provided dataset.
The dashboard should consist of:
title
title (label) of the parameter
parameter that takes values from 5 to 20 (in increments of 5), and determines the number of countries shown in the charts.
two visualizations from the first point, placed side-by-side
To run the dash application in Google Colab, use the solution presented in the course, based on the threading and google.colab libraries. Use the function that displays the application in a new browser tab.

