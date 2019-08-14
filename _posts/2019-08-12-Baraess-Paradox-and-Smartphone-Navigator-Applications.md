
Probably all of us, if we have a car, use navigator applications to find the fastest route. Especially when there is a huge traffic in the city. (In our country), people usually use Google Map in the past. But just recently, there is a large number of new applications that are far better than Google Map, usually because of their new features such as navigation guidance voice, online update, better estimation, etc. <br>
 
Two years ago, those applications were doing quite well. But nowadays, we have a very strange type of traffic in our city. When you drive in the afternoon, you will see that some highways are completely congested while some others are pretty empty. I think this situation is similar to a concept that I have learned in Game Theory. I want to discuss it here: <br>
 
## Let’s talk about the competition between navigation apps first:
 
Of course, all of the navigator applications try to maximize their customers by providing better features. One of the most important features is **ability to find the fastest route for each customer**. So the applications are written in a way that if there is a better shortcut, that shortcut will be get used for customers to tempt them to use the same application for the next time. (instead of any other competitor apps.)<br>
 
As a result, all applications are trying to give the best route for each individual at the beginning of their launch. And because there is competition between different companies, this process will not change. They will always give the best way for each individual. <br>
 
People use the best applications, so if there are several applications, they should have the same performance on average. <br> 
So basically, aside from the specific application that each individual uses, each individual is trying to find the best route for himself. <br>
## Let’s define Average Travel Time
In this setting, each person has an average travel time. (Since we don't have any information about each individual, and because, roughly speaking, each region in the city is similar to other regions, we can assume that the situation for each individual is the same and symmetric, so this average time is the amount of time we need to put for each travel) <br>
There is a question arising in this setting. Using this app necessarily leads our city to have the lowest possible average travel time? Can we do better? <br>
Someone might think that if each individual tries to minimize his travel time in each travel, then he is using routes less than the time when he doesn't. So on aggregate, this will be the best possible choice for each individual. But this is not necessarily true. (I know it might be a little confusing for the first time, but wait), I will explain it using a very famous example which is called Baraess Paradox. 
 
## Baraess Paradox
(All of the images here are from Game Theory Alive book [1])
Suppose that we have 2 routes from A to B similar to the image below. Each edge in this graph has a latency function. We call it $l_e(x)$ where x is the amount of cars in that edge. <br>
Here, edge AD and CB has a constant latency function equals to one. $l_(AD)(x)= l_(CB)(x)=1$ (they are streets which are sparse enough so that you can drive with the maximum speed of 30km/h without any trouble.) <br>
Edge AC and DB have a latency proportional to the number of drivers that currently use that edge.$l_(AC)(x)=l_(DB)(x)=x$  (You can assume that they are highways. On highways, you should keep your distance with the car in front of you in a way that if it immediately stopped, you would be able to react properly and stop your car. And the distance with that car is proportional to the number of cars using that route. i.e. If there are x cars on the highway, on average the car in front of you have d meter distance with you,
on the other hand, if there are 2x cars, then on average the car in front of you have d/2 meters distance from you. so you need to decrease your speed from v to v/2 to keep your time distance with the car. as a result, the latency will increase from t to 2t.)<br>
 
So in this setting, AC and DB are highways and we love to use them!

![city-1](https://raw.githubusercontent.com/AliMorty/AliMorty.github.io/master/images/city-1.png)

 
## What will happen in this setting?
Ok so in that setting, what will happen?
Suppose that 100*x percent of drivers like the top route and 100*(1-x) percent like the bottom route, then if $x\geq 0.5$ after a few days, those drivers who like the top route will notify that the bottom route is better, so they will lose their interest as the time goes on. So we will see a decrease in the x population. If we plot the population for the top route each day, we will probably see a sequence converging to 0.5.
If the $x\leq 0.5$ same things happen to bottom route drivers. <br>
 
So, after few weeks, our expected latency would be: <br>
1 + 0.5 for both top drivers and bottom drivers.
 
 ## Adding a new road is not always good
Now suppose we construct a shortcut from C to D with latency zero. Of course, adding a new line with no latency seems a good idea. People would love this. Because they can use the path A-C-D-B to use both of the highways. (Adding this shortcut is very similar to the situation in which people have access to a navigator app that knows local shortcuts from a highway to another. The app gives the best possible map for each individual that uses it)
 
Forget about the navigator app for a minute and suppose we are about to add our zero-latency shortcut.

![city-2](https://raw.githubusercontent.com/AliMorty/AliMorty.github.io/master/images/city-2.png)
 ### What will happen?
The day after we construct this shortcut, the drivers of the top route will notify that A-C-D-B is a faster route. So they will become interested to change their path. They will use A-C-D-B and the DB highway will become more crowded. As a result, the bottom drivers (A-D-B) will try to use the top route (A-C-D). As they use it, they will notice that there is a new shortcut C-D. They will test it and they will realize that the best path is A-C-D-B. Finally, after a couple of weeks, all drivers will use A-C-D-B as their path. (Infact, this choice is a **Nash equilibrium**, meaning that after a day, nobody will have any regret about the path he chose, also note that there might be several Nash equilibria)
It means that all of the drivers use two highways and as a result, we have two crowded highways that are like streets. It is like there is no highway at all! That’s a tragedy! So **adding a shortcut is not always a good idea**.
![congested](https://raw.githubusercontent.com/AliMorty/AliMorty.github.io/master/images/city-3.png)
 
## Getting back to our navigation problem
Adding a shortcut is in some sense related to the use of this navigation applications. Sometimes they give us shortcuts to get away from congested traffic. But it doesn’t necessarily mean that what we are doing to the traffic will not make the condition worse even for ourselves. Of course, this example is a very simplified model that cannot capture all the properties of a city. These linear latency functions are good to model network connection and not necessarily the best choice for traffic in cities. But aside from these simplicity making assumptions, there is a fundamental flaw when all people try to only maximize their objective. This might be the case that the <br>


>> The best for the group comes when everyone in the group does what’s best for himself AND the group.<br>


In the game theory community, people try to find a bound on how bad it is for people to be selfish comparing to the best average result. They will call this bound **price of anarchy**.
## Price of Anarchy
In the above example, the price of anarchy is: <br>
$$ \text{price of anarchy} =: \frac {\text{average travel time in the worst Nash equilibrium}}{\text{average travel time in socially optimum outcome}}=\frac{2}{\frac{3}{2}}=\frac{4}{3}
$$
So if we live in this simple city, we can ask all people to not use the shortcut, as a result we can have a better travel time. Ok. Let’s talk about a better model for traffic. 
###  A better model
I saw this model from Section 8.4 Atomic Selfish Routing from [1] (which is a very great book, at least for me). This model is closer to our city. <br>
I brought the definition of it from [1]: <br>


>> Consider a road network G = (V;E) and a set of k drivers,
with each driver i traveling from a starting node $s_i \in V$   to a destination $ t_i \in V$ .
Associated with each edge $e \in E$ is a latency function$l_e(n) = a_e . n+b_e$ representing
the cost of traversing edge e if n drivers use it. Driver i’s strategic decision is which
path $P_i$ to choose from $s_i$ to $t_i$, and her objective is to choose a path with minimum
latency. <br>





 
## To what extent we can hope for a better application
In General, if we have n drivers, each i wants to drive from $s_i$ to $t_i$ and all routes have linear latency function, then the price of anarchy is at most %\frac{5}{2}%. Meaning that if we use the best social optimum paths, then the best thing we can hope for is to decrease our average latency by the factor of \frac{2}{5}. This is a bound on how bad the navigation apps affect the traffic compared to the best possible routing system.  
 
## How we can achieve this best possible  
 
 
 
 
As we use different apps, and because they are competing with each other, they will give you the best possible route which maximizes only your objective. If all applications tri
 
## How bad it is?
 
 
 
 
 
So, as you see in this example,
 
 
 
 
 
 
 
** Sometimes, using some navigators app is similar to adding some shortcut with very little latency. ** So it seems harmless to use those apps.
 
In general, we can assume that the latency in each edge is linear with respect to the proportion of population (x) who uses that edge:
$$ l_e(x) = a_e x + b_e $$
 
 
 
 
This situation is, of course, familiar in Game Theory community! Christos Papodimitroiv et al. call this Price
 
 
TODO: mention beautiful mind sentence when John Nash is in the bar: the best result come from a group who chooses the best setting that is better for the group not for each individual!
 
TODO: add a payment function if a person wants to use individual optimum rather than social optimum
 

