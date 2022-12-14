CS50 Final Project
# F1 Telemetry
## Video Demo:  https://youtu.be/eIqGAvmENlA
#### Description:
  
  Hello CS50! My final project is called F1 Telemetry, and it is meant as a tool for comparing drivers' performance to one another by displaying a visual representation of various data-points collected throughout each session.
  
  To do this, I am pulling information from the fastf1 python package. Fastf1 has a vast collection of historical data on Formula 1 events. From fastf1's documentation: "fastF1 gives you access to F1 lap timing, car telemetry and position, tyre data, weather data, the event schedule and session results". Fastf1 is also designed around Matplotlib, which opens up various opportunities for creating the data visualization used on this final project. 
  
  The project was written using Jupyter Notebok, and is rendered as a standalone web application using the Voila extension. Ipywidgets were used for visualization and interactive browser controls. 
  
  The first new thing I had to learn was what was available to me from fastf1's objects and methods, and how to use matplotlib's functionalities for creating intuitive data visualizations. I studied fastf1's documentation thoroughly and after experimenting with retrieving various different data points and creating visualizations, I started to focus on what I really wanted my web application to display.
  
  Originally I had my application display only the plots created by matplotlib, however, fastf1 has to sort through an enormous amount of data to create the plots. Caching is enabled to speed up the process. However, if any data is being downloaded for the first time, it can lead to an extended wait period before the plots are displayed. For this reason I chose to not only display the plots, but also display the output from loading data from fastf1, so that users might get a sense of what is happening while information is being retrieved, instead of waiting in the dark for the plots to be displayed, unsure of whether the application is doing anything or not.
  
  One of the main challenges I faced when developing this project was creating interactive browser controls that reacted to the user's previous inputs. For example, when the user selects the year he wants to compare data from, the list of drivers should update accordingly to account for drivers who actually competed that year, so too should the tracks and events be updated to account for different calendars. 
  
  To achieve this I had to monitor for any changes that the user might make to their previous selection. I used ipywidgets' .observe method to monitor for any changes to previous selections.  Once a change is detected, my code uses fastf1's .sessions object to retrieve event information based on the new selection (this can include a string containing the names of drivers who competed that year, or the event schedule for that year, for example). This new information is then loaded into a string and all relevant parts of this string are appended into a list. These new lists are then used to create the new selection options available for the user.
  
  In the odd event that this automatic error correction method fails to produce a valid selection, an error message is displayed informing the user of the invalid selection, prompting them to change their inputs and try again. This can occur, for example, if you try to select a driver who was competing that year, but might have had to sit out of an event due to illness - something that the code will not correct for.
  
  I invite you to play around with the application and find different drivers' stats to compare, and if you follow F1 closely, try to think of a selection that might lead to an error message (a fun easter egg is included with it that F1 fans might enjoy). I had a lot of fun playing with different visualizations in the app and I hope you do as well!
  
  I extend my sincere thanks to all the CS50 staff for this amazing introduction into programming. I'm very excited to continue my development as a programmer. 
  
  Best regards,
  Pablo Reis Geraidine.
 
  
