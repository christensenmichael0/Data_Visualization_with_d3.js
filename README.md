Summary 

For this project I used a 2012 Center for Disease Control and Prevention dataset from 
data.gov which focused on impaired driving death rate in the United States. Impaired, in 
this case, means that a driver involved in the crash had a Blood Alcohol Content (BAC) greater 
than 0.08. I focused my attention on death rate for males aged 21-34 and through a chloropleth 
map visualization, I was able to illuminate spatial patterns in impaired driving deaths for 
this group. The highest death rates occured in the northwest, the south, and the southeast.

--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
Design

I used a chloropleth map to visually encode the state by state impaired driving death 
rate data. I decided to use a 6 class, multi-hue GnBu colorscale that is color-blind safe. 
Using 6 discrete colors most-effectively illustrated spatial patterns in the data with 
the darker shades of blue representing the highest death rates amoungst 21-34 year old males 
involved in a car crash with a driver having a BAC greather than 0.08. States with fatality 
rates based on fewer than 20 deaths are suppressed and assigned a value of N\A (not applicable).
This is illustrated using a solid grey fill on the chloropleth map. To engage the user and
make the map interactive, I wired in a hovering capability where the tooltip provides the state 
name and death rate per 100,000 population.

Below I address some design changes in response to reviewer comments:

Elaine: "It is difficult to tell what states have no data and this is not conveyed in the legend"

* States with no data are now shaded grey and a legend entry has been added. I chose grey because it
clearly identifies the state (whereas as white was difficult to differentiate from the lighter green
also present in the graphic). Making states with no data the color black drew too much attention to them 
and seemed to distract the audience from the true message of the graphic.

Glenn: "The legend could use some work. Its position and labeling could be more explicit."

* I shrunk the legend entries into small square boxes and labeled them more explicitly. I also
shifted the entire legend to the lower right-hand corner of the screen to improve its visibility.

Jill: "What about Hawaii and Alaska? Those are US states why aren't they shown."

* I found and used a different geoJSON data file. Now Alaska and Hawaii are shown even though data
is suppressed for both states. 

--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
Feedback

*Glenn's comments on initial visualization:*

"The legend could use some work. Its position and labeling could be more explicit."

"The map does a nice job at quickly conveying spatial trends"

*Glenn's comments on the final visualization:*

"The legend is more descriptive and easier to read"

"It's pretty clear from the graphic that impaired driving death rate for young males
is higher in the south, southeast, and northwest than in the northeast or west."

"I wonder why the death rate is so much higher in some states." Are the penalites for OUI
less severe?"

*********************************************************************************************************

*Jill's comments on initial visualization:*

"What about Hawaii and Alaska? Those are US states why aren't they shown."

"Where is the dataset from? Can you provide a link to it?"

"The death-rate range on the scale for each color should be shown."

*Jill's comments on final visualization:*

"The states where data were suppressed now stand out to me and make me realize there is less 
information on states in the northeast than I originally believed."

"I can definitely tell that there are regional hot spots were death rates are 
elevated."

"The graphic is well-done and easy to understand."

*********************************************************************************************************
*Elaine's comments on initial visualization:*

"It is difficult to tell what states have suppressed data and this is not conveyed in the legend."

"Representing states with suppressed data using the present colorscale is missleading."

"I don't like the scale being so elongated and tucked away on the left-hand side of the page."

*Elaine's comments on final visualization:*

"The graphic is much improved in the final version."

"The interactively is nice and it really helps me focus in on death rates for specific states."

"I would be interested to see what more recent data looks like and look at the change over time."

--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
Resources 

http://eric.clst.org/wupl/Stuff/gz_2010_us_040_00_5m.json
https://github.com/alignedleft/d3-book/blob/master/chapter_12/us-states.json
https://github.com/alignedleft/d3-book/blob/master/chapter_12/05_choropleth.html
http://catalog.data.gov/dataset/impaired-driving-death-rate-by-age-and-gender-2012-all-states-587fd
http://bl.ocks.org/michellechandra/0b2ce4923dc9b5809922
http://bl.ocks.org/d3noob/8150631
https://www.dashingd3js.com
