# Hockey Project
### Aim: Create a post-match report/dashboard for a hockey coaching team highlighting key actions in the game such as pass map, goal shot map, shooting efficiency and key performers in the games.

Tools used:
- Python for analysis
- Tableau for visualization and dashboard creation

Data Info:
- There are two data files & a rink template for scatter plots. One data file has a condensed event set from a randomly chosen hockey game and the other contains Expected Goals values (xG) to be merged onto shot attempts for this game. **If an xG value does not correspond to a shot event, it should not be counted**

- X and Y Coordinates are in feet and are adjusted such that both teams attack from left (dz) to right (oz)
    - X values range from -100 (end boards behind the DZ net) to 0 (centre ice) and 100 (end boards behind the OZ net)
    - Y values range from -42.5 (west side boards) to 0 (centre ice) and 42.5 (east side boards)
    - **When creating scatter plots, please use these coordinates along with the provided rink_template to display the full rink**

- Binary columns that have values of 0 or 1 indicate 0=No, 1=Yes

- Successfull passes are completed passes, successful shots are shots on net

- Compiledgametime is in seconds, and periods are 20 minutes long, except for overtime which is 5 minutes or less

### Match Report Dashboard
Link to interactive dashboard: https://raw.githack.com/Lekan-E/SportProjects/main/Hockey%20Project/index.html

![Alt Text](https://github.com/Lekan-E/SportProjects/blob/30538c36fe535a8aca65ad4e612d991f59290f22/Hockey%20Project/Tableau%20Images/Match%20Dashboard.jpg)

### Questions
Q1) 
a) Which teamid won the game, what was the score, which period was the winning goal scored in?
b) Limited to the period where the winning goal was scored, create a scatter plot for the winning team's shot attempts in that period and highlight the winning goal in a different colour.

![Alt Text](https://github.com/Lekan-E/SportProjects/blob/931ad96b500b9fb6f299bd054bd2a062492909bc/Hockey%20Project/Tableau%20Images/Q1b.jpg)

Q2)

a) Which playerid scored the winning goal? 
b) Create a scatter plot for all of this player's powerplay shot attempts for the full game.
![Alt Text](https://github.com/Lekan-E/SportProjects/blob/931ad96b500b9fb6f299bd054bd2a062492909bc/Hockey%20Project/Tableau%20Images/2b.jpg)

c) If we told you these were Alex Ovechkin's powerplay shot attempts, what would you need to do to the Y coordinates for these attempts to appear from "Ovi's Office"? Please re-create the scatter plot accordingly.
![Alt Text](https://github.com/Lekan-E/SportProjects/blob/931ad96b500b9fb6f299bd054bd2a062492909bc/Hockey%20Project/Tableau%20Images/2c.jpg)

Q3)
a) The Assistant Coach wants to know how each team's even strength pass completion rate breaks down in each zone (please use the zone of pass origin). Build a simple visual to display this information for them in a clear and digestible way. 
![Alt Text](https://github.com/Lekan-E/SportProjects/blob/931ad96b500b9fb6f299bd054bd2a062492909bc/Hockey%20Project/Tableau%20Images/3a.jpg)
![Alt Text](https://github.com/Lekan-E/SportProjects/blob/931ad96b500b9fb6f299bd054bd2a062492909bc/Hockey%20Project/Tableau%20Images/3a%20(2).jpg)

b) Which zone was more difficult to complete passes in at even strength, why do you think that is? 
c) What was each goalie id's slot save percentage? (the slot includes innerSlot, westOuterSlot, & eastOuterSlot)

Q4)
a) Assuming the centre of the net is at X=89 (goal line), Y=0 (centre ice), what was the average shot distance for each team for shots from the outside north west playsection to the centre of the net?
b) What was each goalie's Goals Saved Above Expected from the outside north west playsection? What does this tell us about their performance from this area?

Q5)
a) If a "Shot Assist" is defined as a sequence of events where there is: 1) a successful pass followed by 2) a successful reception by a *teammate* and then without giving up the puck 3) the receiving player has a shot attempt, create a column flagging shots that have a Shot Assist. How many shot attempts did playerid 7380 have that were assisted?
b) For shots that were assisted, if the full xG value from the shot attempt was credited to the passer for their successful pass (shot assist), which passer created the most xG for their teammates?
c) Plot a single diagram of this passer's shot assists (pass to reception) and their corresponding shots (reception to shot). Hint: Don't forget what you learned about plotting Y coordinates.

Q6)
a) Which team won the xG battle and how much xG did each teamid have?
b) Given who won the game, what does this tell you about how the game went?


