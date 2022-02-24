# Welcome to my Portfolio!

# About
My name is Adam Fong and I'm a 3rd year Integrated Engineering (IGEN) student at the University of British Columbia, Vancouver campus. (If you haven't heard about IGEN before, [click me!](#about-igen)). I love learning practical skills and applying them to new and old problems. My current muse is data analysis but I'm pretty content whenever I have a challenging problem to tackle. When I'm not working on my projects, I love getting outside spending time soaking in the sunshine (or more accurately, rain) in Beautiful British Columbia. 

# Projects

## Active
- [Bike Sentry](#bike-sentry) - 3rd Year Capstone
- [Grapevine Cold Hardiness](#grapevine-cold-hardiness)
- [AgroBot - Weed Extermination Robot](#agrobot)
- [Star Collector](#star-collector) (active but backlogged)

## Archive
- [Brain Signal Classification](#brain-signal-classification)
- [MusicMe](#musicme) - 2nd Year Capstone 
- [Climate Mapping](#climate-mapping)
- [Bike Tour Updater](#mom-updater)
- [Line Following Robot](#line-following-robot)
- [Electric Ukulele](#electric-ukulele)

# Hobbies
- [Road / Gravel Cycling](#cycling)
- [Open Water Swimming](#open-water-swimming)
- [Rock Climbing (indoors and outdoors)](#rock-climbing)
- [Trail Running](#trail-running)

# Detailed Catalogue

## Bike Sentry
### Summary
Bike Sentry is a solution that my capstone team and I have generated to combat an issue that crosses all cyclist's minds - bike theft. Our solution elegantly combined all of the interests of our diverse group members by including non-trivial tasks in software, electrical, and mechanical engineering. The main preventative measure is by allowing cyclists to opt into an alert system which is constantly monitoring their bike while they are away. If any thief wants to cut a U-lock on the bike rack, our microphones will detect the angle grinder and enter theft mode. Our onboard IoT computers will notify all cyclists who have their bikes attached to the rack as well as the authorities of a theft in progress. 

### Contributions
- High level design of software components including, pan & tilt control, object detection, live audio classification
- Collecting data for, researching, and training a binary audio classifier to distinguish between environmental noise and angle grinders
- Deployed binary classifier within a ROS environment on Raspberry Pi which constantly classifies audio snippets from a USB microphone

## [Grapevine Cold Hardiness](https://github.com/afong3/hardiness)
### Summary
For northern wine regions like the Okanagan Valley in British Columbia, freezing events in winter can cause grapevine death and economic losses. Knowing when the air temperature is cold enough to be damaging is of great value as preventative measures can be taken, but at a large cost. Combining the weather forecast and a prediction of the lethal temperature for a grapevine on a given day can be very important in the decision to protect the crop or not. The tricky part about knowing when it's too cold out for the crop is that grapevine's tolerance to cold is dynamic throughout the winter and varies by cultivar, the weather, and more. I'm attempting to predict the lowest temperature that a grapevine located in the Okanagan Valley, BC can survive in based on data from the nearest weather station to the vineyards in Penticton. 

While I do not understand the mechanisms behind how grapevine cold hardiness changes throughout winter, I am using this interesting topic to gain familiarity in different modeling frameworks and learn about ecological processes as a byproduct. My original approach was to come from a black-box, machine learning persepctive. And to complement this I'm taking a more involved, and hopefully interpretable, Bayesian approach.

### Progress
- **Preparation**
- cleaned weather and cold hardiness data 
- created methods to easily manipulate data for feature engineering and add new predictors quickly
- **ML**
- large correlation analysis with different grouping factors to find good predictors 
- prediction for Sauvignon blanc at one vineyard
- **Bayesian**
- learning rstanarm and stan
- data simulation and parameter recovery

## AgroBot
![led_sim_gif](/images/agrobot_led_sim.gif)
### Summary
AgroBot is a UBC Design Team which is aiming to minimize pesticide usage and/or manual labor by automating the weed removal process in crop rows. The robot will straddle a crop row and move down the line. Using computer vision to identify weeds from crops on the ground, an array of pesticide sprayers will dispense pesticide only where it's needed to exterminate the weed. 

My role is to aid in the software implementation of the weed extermination. 

### Progress
- developed robust method to sort a constant feed of weed locations and assign the correct sprayer(s) to spray on time
- simulated weed identification and sprayer actuation in a ROS environment on a RaspberryPi connected to LED's 

## Star Collector
![star_collector](/images/star_collector.png)

### Summary
My love for outdoor sports arose when I first moved to Vancouver, BC. I picked up road cycling, open water swimming, scrambling, trail running, and continued rock climbing. Vancouver is truly a one-of-a-kind location for an outdoor enthusiast. The tough reality of being a "weekend warrior" free weekends become scarce as the school year progresses. Luckily for UBC students, we have immediate access to over 70 kilometers of beautiful trails in our backyard paradise, Pacific Spirit Regional Park (PSP).

I've spent many hours running and biking through PSP and have loved every minute of it - my exercising time in the forest is how I recover from long days. But like all things, the trails that I frequent have become more and more familiar and my drive to get out to the far corners of the park has faded. But I like to throw code at my problems so no worries! 

[Star Collector](https://github.com/afong3/StarCollector) a tool which takes my (and some of my other trail enthusiasts') GPX data from Strava and highlights which trails have and haven't been traveled since a given date. The pursuit of collecting all the stars has been a great motivator and showed me portions of the park that I would have missed otherwise. My code has been written so that I could easily adapt this 'star collection' to be implemented on any trail / road network. This could even be leveraged into a reward system (if this tool was implemented on some social platform)! But for now, it just removes the mental load of deciding what my route will be. All I have to do is go collect a new star and I'll be satisfied. 

### Progress
- Data retrievel from Strava's REST api
- Automatic map generation with red and gold stars for uncollected and collected 

### TODO
- integrate Strava's OAuth2.0 protocol with redirects for any Strava user to use the app
- Attempt to convert this into ReactJS 



## Brain Signal Classification
![muse_1](/images/muse.png =x250)
### Summary
This project was a group project for the Machine Learning (ML) and Artificial Intelligence in Manufacturing course that I have taken. The main goal of the project was to complete a ML project from data collection all the way to validation. Our task was to make a binary classifier to find a difference in brain signal states among our group members. We chose to classify if our members were caffeinated or uncaffeinated. To prevent overstepping the scope of this course by adding too much data collection rigor, we recorded data immediately after drinking coffee and after not having coffee for 24 hours for each of our members. 

After recording all our data, we coded a preprocessing pipeline to analyze n-second windows of the signals - producing aggregate statistics on each window. These features were used to train an ANN, KNN, SVC, and Random Forest classifier to compare accuracy. 

### Outcome
- Familiarity with Google Colab
- Trained multiple deep and non-deep learning ML classifiers 
- Learned how to perform FFT on time series data
- Experimented with feature creation and optimizing calculation speeds
- Experienced how fun it is to contribute to a project from data collection to validation
- Improved familiarity with Numpy, Keras, SciKit-learn

## Climate Mapping
### Summary
### Outcome

## Mom Updater

### Summary
### Outcome

## Line Following Robot
![lfr_1](/images/line_following_robot_1.jpg)
![lfr_2](/images/line_following_robot_2.jpg)
![lfr_3](/images/line_following_robot_3.jpg)

### Summary
### Outcome

## Electric Ukulele
![uke_1](/images/electric_ukulele_1.JPG)
![uke_2](/images/electric_ukulele_2.JPG)
### Summary
### Outcome

## [MusicMe](https://erikdahl.ca/apps/musicme/#/)
### Summary
MusicMe was our 2nd year capstone team's attempt at merging text tone analysis and music recommendations. Any Spotify user can sign into the webapp, enter their thoughts, and have a song based on their input's tone. We also added some fun features such as picking a random song from our database. The recommendations are far from perfect but this was the first larger software project I've been able to work on.

### Role/Outcome
- Set up a Google Firebase database which stored user and song data
- worked on the API calls to IBM tone analyzer 
- Introduction to OOP

## Cycling
### Bellingham, WA to Williston, ND Bike Tour (3000 km)
![bike_tour_map](/images/bike_tour_final.png)

### Summary
From July 15, 2021 to August 15, 2021 I was on a bike tour from Bellingham, WA to Williston, ND with four friends. I cycled 3,000 km's, entered three time zones, and spent the night in nearly 30 new locations. The summer of 2021 was a terrible year for wildfires and our route had been detoured a few times to avoid them. Not having a plan set in stone was liberating after having a year of a rigid, online school, schedule. The generosity of strangers, the small towns I passed through, the pace of travel, and the camaraderie made this trip unforgettable. I'm looking forward to the next time I'm able to travel by bike. 

## Open Water Swimming

## Rock Climbing

# About IGEN 
[Integrated Engineering](https://www.integratedengineers.ca/) is a one of a kind, group-project focused, and interdisciplinary engineering degree in which students learn fundamental engineering concepts in each of the classical disciplines. Not only do we get to work on a year long capstone in our 2nd, 3rd, and 4th years - we think of and propose the projects, giving us experience in concept generation and effectively pitching our ideas to our peers. 

Our multidisciplinary foundation is supplemented by choosing a major and minor discipline to further study after tasteing a bit of each engineering flavor. Each student can take a unique educational route, making our group projects substantially more interesting than a capstone filled of 5 students from the same discipline. 




