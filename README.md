# Semester 1 Capstone Project 

## Project Overview

        In this project we performed exploratory data analysis and used statistical methods to provide business insights to Computing Visions for recommendations on movie performance based off availible data. We provided three different recommendations, including the movie production budget, movie genre, and movie release month.

## Business Understanding

* Include stakeholder and key business questions

Stakeholder - Computing Vision

Business Question - What movie attributes will help create a successful movie?

## Data Understanding and Analysis
        
* Source of data
IMDB
The Numbers

* Description of data
IMDB - Movie title, movie genre, movie actors
The Numbers - Movie title, movie release date, movie worldwide gross, movie production cost

* Three visualizations (the same visualizations presented in the slides and notebook)
Production Budget
![image](https://user-images.githubusercontent.com/108894241/185704096-6172eb51-4c9f-40d0-92ff-155384144dcc.png)
Movie production budget vs. Worldwide Gross of the movie. We can see the positive correlation between the two
![image](https://user-images.githubusercontent.com/108894241/185704128-5f203ed9-59ca-4bd8-9158-d119495a4809.png)
Most popular actors in most grossing movies. Popular actors grant visibility and therefore higher gross. 

Genre
![image](https://user-images.githubusercontent.com/108894241/185704170-7c0f0fc4-4199-425c-87b2-e026464bef1c.png)
Median Worldwide Gross by Genre w/3rd quartile line. The three highest grossing genres were Animation, Adventure, and Action
![image](https://user-images.githubusercontent.com/108894241/185704185-25873803-9ec5-49d4-ac11-45759962bc6f.png)
Distribution of Worldwide Gross for Animated vs. Nonanimated movies. Animated movies significantly perform better than other genres.

Release Month
![image](https://user-images.githubusercontent.com/108894241/185704195-9b99efd4-23bd-4c33-a00d-f7644d32502d.png)
From the graph above, we can see that the average gross earnings is significantly higher during the holiday seasons.
![image](https://user-images.githubusercontent.com/108894241/185704213-132f1678-1c87-4812-b43c-6e086c38b029.png)
Animated movies released in the month of June yielded highest average gross earnings.
![image](https://user-images.githubusercontent.com/108894241/185705106-3679a219-ea6d-4f02-ac0b-7e3b015a24f5.png)
We can see that May has returned highest average gross earnings for Adventure movies, but having a very similar pattern to the Animated movies release time.

## Statistical Communication

Statistical Communication
We performed a 1 sample t t-test.

Alpha = .05

H0: Sci-Fi Movies produce the same World Wide Gross as other genres of movies
HA: Sci-Fi Movies produce a higher World Wide Gross than other genres of movies

Rational
We are using a hypothesis test to determine if there was a significant difference between the Worldwide gross of Sci-Fi movies compared to the rest of the sample of movies. We used a 1 sample t-test instead of a graph so that we could see if the difference was statistically significant. 
With a p-value that is approaching 0, we can reject the null hypothesis

Limitations
The largest issue that comes here is due to the skewness of the data. This is likely due to the data collection hear, as the database with the production value and worldwide gross only has around 4k movies, compared to the 150k+ movies on the IMDB database. These movies also appear to be larger movies that have a much higher production value.

Recommendations
We would recommend that the company creates a sci-fi movie, as it has the highest return, and is statistically significant compared to the others.


## Conclusion

After performing our analysis we were able to come to 3 conclusions for movie attributes that Computing Vision should consider when producing their movie.

Production Budget
After comparing production budget and worldwide gross, it was found that having a higher production budget can yield higher total gross.

Movie Genre
From the analysis, the top profitable genres are Animation, and Adventure. Computing Vision should create a movie that incorporates these genres.

Release Month
Performing analysis showed us that Computing Vision should release Animated movies in the months of June or July and an Adventure type movie in May or June .
