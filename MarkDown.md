"Highest Grossing Movie Analysis (2008-2018)"

![moviereel](https://github.com/marbwhist/first-project/blob/master/filmreel.png?raw=true)

***To Begin

First we had to source our data:

    1. We started by finding a csv file on Kaggle that showed all of the highest grossing worldwide movie sales from the last 50 years.  
    2. We narrowed down the data by pulling only films that were released in 2008 or later.  
    3. We further narrowed down the data by pulling only films that grossed over $100mil to find the true top blockbusters.  
    4. We used the OMDB API to fill in the Metacritic scores, cast names, and film synopsis  
    
***Answering our questions

*Are there any recurring themes of the plots of the highest grossing movies 2008-2018?

Processes:
    1. Create an empty master list to hold our all the words  
    2. Create a for loop to run a split on the string in the synopsis column  
    3. Add the synopsis words into the new master list  
    4. Create an empty list to count the words  
    5. Create a for loop to run the word counter in the master list and count the most recurring words  
    6. Zip together the word count key and word count list, and add the words to the word counter list  
    7. Make a new data frame to hold the words  
    8. Create a for loop for the value counts of most occuring words  
    9. Typecaste each value to string and split the value  
    10. Convert all to lowercase  
    11. Create the word cloud and plot  

Answers:
    1. When  
    2. World  
    3. Must  
    4. New  
    5. Find  
    
![worldcloud](https://github.com/marbwhist/first-project/blob/master/plot_word_cloud.png?raw=true)


*What were the most profitable actors/actresses in the same movies?

Processes:
    1. Find mean, median, and mode on the worldwide gross numbers  
    2. Used the if function to add the cast members to a list  
    3. Used the explode function to separate each actor into their own row into a new dataframe  
    4. Created a summary of average sales, IMDB rating, and Metacritic for the films each actor was in  
    5. New dataframe with this data with the actor's name being the index  
    6. Create a new table for the actors who were in more than 1 movie  
    7. Showed the top ten high grossing actors with more than 1 movie and sorted by average worldwide gross sales  
    8. Made a bar chart showing the top 10 actors by gross movie sales  
    9. Made a bar chart showing the top movie studios by gross movie sales  
    10. Create a new table to show movie sales and ratings averages by movie title  
    11. Made a bar chart to show gross sales per movie on the top 10 grossing films  
    
Answers:    
    1. Zoe Saldana  
    2. Michael Gambon  
    3. Christian Bale  
    4. Johnny Depp  
    5. Josh Duhamel  
    
![actors](https://github.com/marbwhist/first-project/blob/master/avg_sales_per_actor.png?raw=true)

![studios](https://github.com/marbwhist/first-project/blob/master/avg_sales_per_studio.png?raw=true)
    
*Which scoring model is most reflective of the financial success of the movie?
 
Processes:
    1. Made a new dataframe to hold the rating results and also adjusted ratings to be on the same scale (1-100)  
    2. Created a scatter plot for IMDB vs Metacritic  
    3. Made bins for worldwide gross and put into a new table  
    4. Created scatter plot to show worldwide gross earnings vs IMDB rating, Metacritic rating, and Average rating  
    5. Made a chart of correlation between ratings and earnings  
    6. Made a chart of correlation between ratings and earnings bins  
    7. Made a box plot by gross group for each rating system  

Answers:    
    Inconclusive results on if one ratings system is more correlated with financial success, however we can see that in general IMDB
    ratings are more favorable than Metacritic

![ratingsscatter](https://github.com/marbwhist/first-project/blob/master/avg_rating_vs_earnings_scatter.png?raw=true)

![ratingvsearnings](https://github.com/marbwhist/first-project/blob/master/avg_rating_by_earnings.png?raw=true)

*What are the most profitable movie genres?

Processes:
    1. Made new dataframe showing only the Genre, Year, Title, and worldwide gross Earnings  
    2. Created a bar chart with Year and Genre grouped, and used the sum function on the Earnings column  
    3. Created a bar chart grouping only by Genre, and used the sum function on the Earnings column  

Answers:
    1. Fantasy  
    2. Sci-Fi  
    3. Action  
    4. Animation  
    5. Comedy  
      
![ratingsbygenreandyear](https://github.com/marbwhist/first-project/blob/master/genre_earnings_by_year.png?raw=true)

![ratingsbygenre](https://github.com/marbwhist/first-project/blob/master/genre_earnings_overall.png?raw=true)