Fork to attempt to add images/add a glow effect. not currently working, will work on it. (4/21)

---------------------------------------------------------------------------------------------------


Fork to add about page (Nick Barton 3/31)





--== PLANET SEEKER ==--        

Created by:
Angelo Ragucci (project organizer)
Nicholas Barton
Justin Robles

A website created to track information about the planets in our solar system.
Uses real time NASA data from the Horizon API to display information about each planet.
Draws phase angles for each planet as viewed from Earth, similar to Lunar phases

Challenges and thought process during creation:

Angelo:
When embarking on this project, I had very little experience writing in javascript,
let alone how to use an API.

I was repsonsible for the javascript portion of this project, which handles
a majority of its functionality, as the idea of this website was somthing I came
up with for our web development group project.

The first hurdle was creating a system that would display the planet along
with its lit portion, that could display any phase angle. I initially tried
describing what I wanted to Claude, however did not acheive the result I wanted.
To remedy this, I tried a new approach. I did this by looking at websites that 
showed the lunar phases, then gave Claude the link and told it make a simple function
that can draw the phase angle and that could take numeric imputs that could later be 
called from an external API. I did this to ensure I could easily change things in the future if needed.

After creating the first prototype that satisfied my vision, I asked Claude to then break down the code.
I made it explain line by line, what everything did, peice by peice in order to understand how it worked.
This greatly helped, as it explained how it made a blank canvas, used a math expression to draw an ellipse,
showed me where I could change the colors, etc. Knowing how this simple function worked allowed
me to debug the code numerous times throughout the project, and tweak minor things to my liking.

Once the system for visualizing the phase angles was implemented, I then moved to retreive the data
from JPL's Horizon API, which is an extensive database of objects tracked in realtime by NASA. The database tracks
a variety of metrics about every single object NASA tracks in space, with time series functionality.
I chose this because it made the program more modular and expandable, allowing me to add additional data
and program addittional content to my liking in the future.

The APi was challenging to work wih at first, as a simple fetch request within javascript returned a CORS error.
I then researched this and how to get around it, and figured out I could use a proxy to connect, thus
bypassing this issue. I then tested its functionality in the console to confirm it worked.

Following this breakthrough, I moved on to parsing the data returned by the API call. This was one of the hardest 
challenges faced during the project, as the API returned its information in a raw text file, making it much more
difficult to search for a specific data point. i eventually solved this by figuring out I could simply convert the
file to JSON format, then having the code sort through the text and pull what I need.

From here, things become much more smooth, as once the API data was pulled, all that was left was to pass that value
to the draw function. This was the last major technical hurdle, and after this only relatively minor visual
and aesthetic changes were made, as the system structure proved quite modular, allowing easy expansion when needed.
An example of this is that the planet speed was added late into the project, but was simple since the foundation was in place.

More features may be added in the future as needed.

