The Data Behind R.A. Dickey
======

Explore every pitch by the Blue Jay's new pitcher R.A. Dickey.

Coding, design, layout, data crunching and writing by Stuart A. Thompson

See the full version here: http://www.theglobeandmail.com/sports/baseball/the-data-behind-ra-dickey-a-pitch-by-pitch-breakdown-of-his-2012-season/article10623044/

Nominated for best Data-Driven Application at the 2013 international Data Journalism Awards: https://review.wizehive.com/voting/view/dja2013/14521/1244473/0

Data via MLB ADVANCED MEDIA


The project and its major findings
-------
This project reconstructs every pitch thrown by R.A. Dickey during the 2012 season — nearly 3,500 pitches in all. Using data from PitchFX tracking software, we were able to determine the exact location of the ball in relation to both home plate and the pitcher’s hand. This allowed us to reconstruct the trajectory of the ball while adding meta data such as pitch result, pitch type and speed.

The resulting interactive discovered many interesting things about the knuckleball pitcher. He throws the knuckleball nearly 85 per cent of the time, but favours the fastball more often on the first or fifth pitch in the count, reaching his maximum velocity in the seventh inning. He’s twice as likely to throw a fastball against a right-hander as opposed to a lefty. 

The data application also lets readers search any pitch according to all available metrics. They could search for all fastballs from the second inning on the third pitch to left-handed batters on the opening game of the season.

Data used and how we obtained it
-------
The data was provided by Major League Baseball Advanced Media, the statistics division of MLB. They worked with us to return the most valuable fields, including X, Y and Z coordinates at the moment of release and when it crossed the plate. The data needed to be refined because the result of any given pitch was stored across two columns.

What were your resources for this project (number of people, budget, time needed...)? *
A multimedia editor mined the data for information and designed the interactive over the course of three days. Several editors were involved in shaping the content and the direction of the interactive. The data was provided free of charge by the MLB.

Techniques and tools used
-------
The data explorer tool was created in Javascript using the Raphael library. Two sets of coordinates were used from the data: first, the X and Z (horizontal and vertical) position were used to place the ball at the time of release. A path was created connecting it to the X and Z position at the plate. The ball’s size and height were adjusted for perspective, since the interactive looked from the perspective of the batter.

A query function was created to iterate through the search form (or any custom query we created) and return only the relevant results. To create the animation, each ball was mapped on the canvas according to its position in the pitcher’s hand. Then a time interval began ticking, animating each ball to the corresponding final position, with a delay on each ball. A second shape was created over the ball to colour-code the result of the pitch according to ball, strike or hit; this was faded above the ball after a short timeout function. Each ball was also pushed into an appropriate array so the results could be filtered later according to ball, strike, hit or player name.

A second piece of the visualization shows how a knuckleball works. This was also created in Raphael. The balls were animated using two images: one of the ball, another of the shadow. Though barely noticeable, this allows the shadow to remain in place as the ball spins, keeping visual accuracy.

A third piece of the visualization breaks down the pitcher’s best game ever: the second of two one-hitters. We plotted the pitches from each inning side-by-side using our custom search function, letting readers replay the game through each pitch. Readers could then toggle the visibility of each batter to see how he fared against R.A. Dickey.