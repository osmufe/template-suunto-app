# Suunto App Template
Suunto App Template 1.0 Version

This template is intended for five fields on the clock screen. One field in the SA Outputs and another field in the SA Summary Outputs. 
 
### HTML Variables & Data:
In the h.tml you have four variables that I have defined in the manifest.json. In the manifest.json I have defined two to save in the SA, two to be able to analyze later in each turn, and the other one for the summary.


## OUTPUT Variables:
Field just under the title, left side: ***Variable climbAttemptAscent***

Field just under the title, right side:  ***Variable climbDurationAscent***

Middle left side:  ***Variable climbAttempts***

Middle right side: ***VariableclimbAngleAscent***

Bottom text area: ***Value of /Activity/Activity/-1/Duration/Current***

## IN Variables:
This variables I use in manifest.json to obtain data from the watch and later play with the main.js

DurationAscent
DurationDescent
AscentMeters
DescentMeters
Distance

## main.js :
You can define variables in main.js to make calculations , or other type of things.

# SA Sumary example
This example funcion returns the data to the SA Sumary with the climbAttempts variable.
function getSummaryOutputs(input, output) {
   return [
     {
      // Save the data of number of times you make a route or ascent/descent in indoor climbing into SA.
      id: 'climbAttempts',
      name: "Number of Ascent",
      format: 'Count_Threedigits',
      value: output.climbAttempts
     },

   ];
 }

 ## manifest.json:

 This exame returns the data in the SA:

     {
      "name": "climbAngleAscent",
      "log": true,
      "shownName": "Angle of Ascent",
      "format": "Count_Threedigits"
    }

  Later in the main.js if you save the value in the variable each time the suunto generate the average in the SA.


### SA Outputs Example:
  #### Suunto Plus Metrics to analize later in SA
  <img src="SuuntoPlusMetric.jpg" width="35%" height="35%">
   <br/>
   
  #### SA Summary Outputs Example
  <img src="SA_Metrics.jpg" width="35%" height="35%">
   <br/>   

---
### :fire: My Stats :
[![GitHub Streak](http://github-readme-streak-stats.herokuapp.com?user=osmufe&theme=submarine-flowers&hide_border=true&date_format=j%20M%5B%20Y%5D&mode=weekly&border=DD2727)](https://git.io/streak-stats)
