# Phase 1 Project




# Project Overview


## Business Problem

Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

## The Data

In this project, datasets from the following were used:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [The Numbers](https://www.the-numbers.com/)

The files were in different formats. Box Office Mojo and The Numbers were in compressed CSV (comma-separated values) files that were opened using pandas `pd.read_csv`, while the data from IMDB was located in a SQLite database. The SQL database had the following map: 

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Only the movie_basics, movie_ratings, directors, and persons tables were used.


## Three Key Factors

Throughout this project, 3 key factors were focused on that can help determine if a movie does well in the box office:

* Genre of movie
* Production budget of film
* Partnering with another movie studio


## 1. Genre of movie

For the first factor, I looked at what kind of movie genres were most popular. I used data from an IMDB database which contained over 85,000 movies along with their ratings, number of people who voted on the rating, the movie director, etc. I looked at which genre had the most movies produced, and which genres had the highest average rating. By far the most produced type of movie was in the Drama genre, which accounted for almost half of the total movies in the dataset. The highest average movie ratings for a genre belongs to the documentary genre, but is closely followed by the sport, musical, history and biography genres.


![frequency of movie genre](https://user-images.githubusercontent.com/45251340/174701111-4b2dd757-829c-479e-8755-72fd29575b22.png)


![average rating per genre](https://user-images.githubusercontent.com/45251340/174701120-f8455400-ad67-4a00-9124-13e3c6666025.png)


## 2. Production Budget

Next, production budget was looked at. I took a dataset from The Numbers, which contained various movies,their production budget and their domestic and global box office earnings. I ran a Pearson's correlation test on production budget and both box office earnings and found a strong positive relationship between production budget and both types of box office earnings, which suggests that a high production budget is correlated with higher box office earnings. I also looked at the average production budget which $31,587,757 with a standard deviation of $41,812,076.


***Here the correlation between production budget and worldwide box office earnings is shown, with a correlation of 0.748***



![worldwide box office correlation](https://user-images.githubusercontent.com/45251340/174701413-31cc6ec0-58c8-4247-9775-b2bcfea7f272.png)



***Here the correlation between production budget and domestic box office earnings is shown, with a correlation of 0.686***


![domestic box office correlation](https://user-images.githubusercontent.com/45251340/174701419-da645fe0-1ca3-4734-a53e-dd0a08b0b35c.png)



## 3. Partnering With Another Studio

Lastly, I looked to see which movie studio would be the best to work together with when producing a movie. I took a dataset from Box Office Mojo which contained over 2000 movies. Each entry had the domestic/foreign box office earnings as well as the studio that made the movie. To determine which studio was the best choice to partner with, I looked at the number of movies each studio produced, as well as the average worldwide gross made by each studio. For number of movies produced, the results show that the top producers of movies are Universal, Fox, and Warner Brothers. I then looked at which movie studios had the highest average worldwide grossing movies, and by taking into account both number of movies and average worldwide gross made by each studio, I was able to eliminate certain studios, and the final choice was Warner Bros Studios. 
 


![movies made by studio](https://user-images.githubusercontent.com/45251340/174701990-ce9507bf-02ba-4e2a-b65a-e6ad1f78bab1.png)
 

![worldwide gross per studio](https://user-images.githubusercontent.com/45251340/174702152-d97306cf-9ce3-4f9a-b2fe-accc1a6c859c.png)


## Summary

3 factors to focus on for a successful movie were suggested:
* Genre of movie
* Production budget of film
* Partnering with another studio


Analyzing each factor and multiple datasets, here are a few suggestions:

* Based on the massive amount of movies in the drama genre produced, using high rating genres that can incorporate aspects of drama would be wise. Therefore the best genres to focus on would be sport, history or musical.
* For production budget, the ideal budget to maximize profits would be between 100 and 200 million dollars. We’ll consider the movie successful if the gross box office earnings are at least twice the production budget.
* Lastly, you should partner up with Warner Bros, a highly experienced and skilled studio that has put out many high grossing box office hits.


