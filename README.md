# F1 Telemetry
CS50 Final Project

# F1 Telemetry
## Video Demo:  <URL HERE>
#### Description:
  
  Hello CS50! My final project is called F1 Telemetry, and it is meant as a tool for comparing drivers' performance to one another by displaying a visual representation of various data-points collected throughout each session.
  
  To do this, I am pulling information from the Fast F1 python package. Fast F1 has a collection of historical data on Formula 1 events. From Fast F1's documentation: "FastF1 gives you access to F1 lap timing, car telemetry and position, tyre data, weather data, the event schedule and session results". Fast F1 is also designed around Matplotlib, which opens up various opportunities for creating the data visualization used on this final project. 
  
  The project was written using Jupyter Notebok, and is rendered as a standalone webpage using the Voila extension. Ipywidgets were used for visualization and interactive browser controls. 
  
  One of the main challanges I faced when developing this project was creating interactive browser controls that responded the the user's previous inputs. For example, when the user selects the Year he wants to compare data from, the list of drivers should update accordingly to account for drivers who actually competed that year, so too should the tracks and events be updated to account for different calendars. 
  To achieve this I had to monitor for any changes that the user might make to their previous selection. I used ipywidgets' .observe method to monitor for any changes to previous selections.  Once a change is detected, my code uses Fastf1's .sessions object to retrieve event information based on the new selection (this can include a string containing the names of drivers who competed that year, or the event schedule for that year, for example). This new information is then loaded into a string and all relevant parts of this string are appended into a list. This new list is then used to create the new selection options available for the user.
  
  
