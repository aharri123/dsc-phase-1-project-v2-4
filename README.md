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
* Building on nostalgia or sequels


## 1. Genre of movie

For the first factor, I looked at what kind of movie genres were most popular. Using data from Statista.com I found that between the years of 1995 and 2022, the most popular genre was action, followed by adventure, then drama. This is shown in the figure below, where total revenue (in billions) represents the success of a genre.

![genres](https://user-images.githubusercontent.com/45251340/171091151-855764e1-eae6-4321-b20e-5dddea2a6e0b.JPG)

I also looked at an IMDB database which contained over 85,000 movies along with their ratings, number of people who voted on the rating, the movie director, etc. Looking at the top most voted for movies, a trend was noticed where most of those movies fell into the action, adventure and drama genre.The results can be seen below.

![genresPie](https://user-images.githubusercontent.com/45251340/171091841-fb1c86ed-7a64-45b4-9181-321fbb99318d.png)

Lastly, I looked at the top 10 lifetime grossing movies, and all of them were in the action and adventure genre, with the exception of one movie, which was in the drama genre. 

![image](https://user-images.githubusercontent.com/45251340/171093670-57868b69-aa24-4302-a8ff-30aad0eae4ec.png)


## 2. Production Budget

Next, production budget was looked at. I took a dataset from The Numbers, which contained various movies,their production budget and their domestic and global box office earnings. I ran a Pearson's correlation test on production budget and both box office earnings and found a strong positive relationship between production budget and both types of box office earnings, which suggests that a high production budget is correlated with higher box office earnings. 

***Here the correlation between production budget and worldwide box office earnings is shown, with a correlation of 0.748***

![image](https://user-images.githubusercontent.com/45251340/171094322-d6a0231d-4d4a-4d4c-b6ab-434880a4d323.png)




***Here the correlation between production budget and domestic box office earnings is shown, with a correlation of 0.686***

![image](https://user-images.githubusercontent.com/45251340/171094433-1350214e-6c46-423f-8da0-78a363192966.png)


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

After research and data analysis from various sources, each of these factors have been shown to help improve box office performance provided they are done correctly.  

1. `README.md`
    * A file called `README.md` at the root of the repository directory, written in Markdown; this is what is rendered when someone visits the link to your repository in the browser
    * This file contains these sections:
       * Overview
       * Business Understanding
          * Include stakeholder and key business questions
       * Data Understanding and Analysis
          * Source of data
          * Description of data
          * Three visualizations (the same visualizations presented in the slides and notebook)
       * Conclusion
          * Summary of conclusions including three relevant findings
