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

For the first factor, I looked at what kind of movie genres were most popular. Using data from Statista.com I found that between the years of 1995 and 2022, the most popular genre was adventure , followed by action, then drama. This is shown in the figure below, where total revenue (in billions) represents the success of a genre.

![genres](https://user-images.githubusercontent.com/45251340/171310497-18c99fb2-bd54-492e-97ef-9450ad63bdf3.JPG)

I also looked at an IMDB database which contained over 85,000 movies along with their ratings, number of people who voted on the rating, the movie director, etc. Looking at the top rated and most voted on movies, a trend was noticed where most of those movies fell into the action and adventure genre.The results can be seen below.

![genresPie](https://user-images.githubusercontent.com/45251340/171310568-531653e7-e3c7-4064-a83e-de13088b725d.png)


Lastly, I looked at the top 10 lifetime grossing movies, and all of them were in the action and adventure genre, with the exception of one movie, which was in the drama genre. 

![image](https://user-images.githubusercontent.com/45251340/171093670-57868b69-aa24-4302-a8ff-30aad0eae4ec.png)


## 2. Production Budget

Next, production budget was looked at. I took a dataset from The Numbers, which contained various movies,their production budget and their domestic and global box office earnings. I ran a Pearson's correlation test on production budget and both box office earnings and found a strong positive relationship between production budget and both types of box office earnings, which suggests that a high production budget is correlated with higher box office earnings. 

***Here the correlation between production budget and worldwide box office earnings is shown, with a correlation of 0.748***



![worldwideBoxOfficeCorr](https://user-images.githubusercontent.com/45251340/171315914-51f70a55-ca6e-4e62-b8f2-66c1ad921fa4.png)



***Here the correlation between production budget and domestic box office earnings is shown, with a correlation of 0.686***


![domesticBoxOfficeCorr](https://user-images.githubusercontent.com/45251340/171315932-b838ee0d-3e1b-4fe7-ae9f-424a0a7b853f.png)


Casuses and implications are discussed further in my presentation.


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
