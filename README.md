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

Next, production budget was looked at. I took a dataset from The Numbers, which contained various movies,their production budget and their domestic and global box office earnings. I ran a Pearson's correlation test on production budget and both box office earnings and found a strong positive relationship between production budget and both types of box office earnings, which suggests that a high production budget is correlated with higher box office earnings. 

***Here the correlation between production budget and worldwide box office earnings is shown, with a correlation of 0.748***



![worldwide box office correlation](https://user-images.githubusercontent.com/45251340/174701413-31cc6ec0-58c8-4247-9775-b2bcfea7f272.png)



***Here the correlation between production budget and domestic box office earnings is shown, with a correlation of 0.686***


![domestic box office correlation](https://user-images.githubusercontent.com/45251340/174701419-da645fe0-1ca3-4734-a53e-dd0a08b0b35c.png)



## 3. Building on nostalgia or sequels

Lastly, I looked at how making sequel movies or building movies on nostalgia can impact how it peforms in the box office. I started off Using a dataset from Box Office Mojo which contained over 3000 movies and their domestic/foreign box office earnings. When looking at the top domestic grossing and top foreign grossing movies, I saw a lot of 2’s, 3’s, and colons, all of which are indicative of sequels. Furthermore, the highest domestic grossing movie (“Star Wars: The Force Awakens”) and the highest foreign grossing movie (“Avengers: Infinity War”) were both sequels of well established series.

You can see the trend in both types of box offices below: 

![image](https://user-images.githubusercontent.com/45251340/171095963-7f2489ba-7201-4437-bd51-01c665052268.png)  ![image](https://user-images.githubusercontent.com/45251340/171095979-27cbf598-9d1f-4a59-a361-c8802ac20bc6.png)



I also looked into more detail in two different series which play on nostalgia, and how that affected their success in the box office. The two series were Star Wars, and the Marvel Cinematic Universe movies. Both of these are discussed more in detail in my powerpoint.


## Summary

3 factors to focus on for a successful movie were suggested:
* Genre of movie
* Production budget of film
* Building on nostalgia or sequels

After research and data analysis from various sources, each of these factors have been shown to help improve box office performance provided they are done correctly. For starters making a movie that is in the adventure or action genre is recommended, as those are the top 2 genres in the past decade. A relatively higher production budget is also suggested, which will allow for things like more special effects, better actors, better equipment, etc. Lastly, it is reccomended to make a movie that builds on older movies/movie series, to play on the audience's nostalgia.  

Closing thoughts and suggestions are discussed in the powerpoint, as well as the chance for the studio to ask any questions.
