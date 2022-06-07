

<a ><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ37C6wHOgUVkzvxdvgcDh7RORQHkiqkZIYa8QrAkFCXBq98Duy8HBtSseggWC1J_WWWwo&usqp=CAU" align="right" height="150"/></a>

# Machine Learning Project – Data Science Movie Recommendation System Project in R 🎦🎬

### Aim of Project
Have you ever been on an online streaming platform like Netflix, Amazon Prime, Voot? I watched a movie and after some time, that platform started recommending me different movies and TV shows. I wondered, how the movie streaming platform could suggest me content that appealed to me. Then I came across something known as Recommendation System. This system is capable of learning my watching patterns and providing me with relevant suggestions. Having witnessed the fourth industrial revolution where Artificial Intelligence and other technologies are dominating the market, I am sure that you must have come across a recommendation system in your everyday life. I am also sure that by this time curiosity must be getting the best of you. Therefore, in this Machine Learning Project, I will teach you to build your own recommendation system.

<a ><img src="https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/data-science-movie-recommendation-project.jpg" /></a>

### Movie Recommendation System Project using ML
The main goal of this machine learning project is to build a recommendation engine that recommends movies to users. This R project is designed to help understand how a recommendation system works. We have developed an Item Based Collaborative Filter. This project helped me gain experience of implementing your R, Data Science, and Machine learning skills in a real-life project.

### What is a Recommendation System?
A recommendation system provides suggestions to the users through a filtering process that is based on user preferences and browsing history. The information about the user is taken as an input. The information is taken from the input that is in the form of browsing data. This information reflects the prior usage of the product as well as the assigned ratings. A recommendation system is a platform that provides its users with various contents based on their preferences and likings. A recommendation system takes the information about the user as an input. The recommendation system is an implementation of the machine learning algorithms.

<a ><img src="https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/recommendation-system-project-in-R.png" /></a>

A recommendation system also finds a similarity between the different products. For example, Netflix Recommendation System provides you with the recommendations of the movies that are similar to the ones that have been watched in the past. Furthermore, there is a collaborative content filtering that provides you with the recommendations in respect with the other users who might have a similar viewing history or preferences. There are two types of recommendation systems – Content-Based Recommendation System and Collaborative Filtering Recommendation. In this project of recommendation system in R, we have worked on a collaborative filtering recommendation system and more specifically, ITEM based collaborative recommendation system.


### Dataset used
In order to build our recommendation system, we have used the MovieLens Dataset. You can find the movies.csv and ratings.csv file that we have used in our Recommendation System Project [here](https://drive.google.com/file/d/1Dn1BZD3YxgBQJSIjbfNnmCFlDW2jdQGD/view). This data consists of 105339 ratings applied over 10329 movies.

### Essential Libraries
```recommenderlab```, ```ggplot2```, ```data.table``` and ```reshape2```.

### Retrieving the Data
We have retrieved our data from movies.csv into movie_data dataframe and ratings.csv into rating_data. We used the str() function to display information about the movie_data dataframe. We can overview the summary of the movies using the summary() function. We also used the head() function to print the first six lines of movie_data. Similarly, we can output the summary as well as the first six lines of the ‘rating_data’ dataframe.

### Data Pre-processing
After retrieving data from the ```movies.csv``` and```ratings.csv``` datasets, we observed that the userId column, as well as the movieId column, consisted of integers. Furthermore, we needed to convert the genres present in the movie_data dataframe into a more usable format by the users. In order to do so, we first created a one-hot encoding to create a matrix that comprises of corresponding genres for each of the films. We then created a ```search matrix``` that will allow us to perform an easy search of the films by specifying the genre present in our list.

There are movies that have several genres. For the movie recommendation system to make sense of the ratings through ```recommenderlab```, We converted the matrix into a sparse matrix. This new matrix is of the class ```realRatingMatrix```. We then overviewed some important parameters that provided various options for building recommendation systems for movies.

We observed that the userId column, as well as the movieId column, consist of integers. Furthermore, we needed to convert the genres present in the movie_data dataframe into a more usable format by the users. In order to do so, we first created a one-hot encoding to create a matrix that comprises of corresponding genres for each of the films.

### Collaborative Filtering - Exploring similar data
Collaborative Filtering involves suggesting movies to the users that are based on collecting preferences from many other users. For example, if a user A likes to watch action films and so does user B, then the movies that the user B will watch in the future will be recommended to A and vice-versa. Therefore, recommending movies is dependent on creating a relationship of similarity between the two users. With the help of ```recommenderlab```, We computed similarities using various operators like cosine, pearson as well as jaccard.

### Exploring Similar Data
Collaborative Filtering involves suggesting movies to the users that are based on collecting preferences from many other users. For example, if a user A likes to watch action films and so does user B, then the movies that the user B will watch in the future will be recommended to A and vice-versa. Therefore, recommending movies is dependent on creating a relationship of similarity between the two users. With the help of recommenderlab, we can compute similarities using various operators like cosine, pearson as well as jaccard.

### Collaborative Filtering System
In this section of the data science project, I developed the *Item Based Collaborative Filtering System*. This type of collaborative filtering finds similarity in the items based on the people’s ratings of them. The algorithm first builds a similar-items table of the customers who have purchased them into a combination of similar items. This is then fed into the recommendation system.

The similarity between single products and related products can be determined with the following algorithm:

- For each Item i<sub>1</sub> present in the product catalog, purchased by customer C.
- And, for each item i<sub>2</sub> also purchased by the customer C.
- Create record that the customer purchased items i<sub>1</sub> and i<sub>2</sub>.
- Calculate the similarity between i<sub>1</sub> and i<sub>2</sub>.

I built this filtering system by splitting the dataset into 80% training set and 20% test set.

### Building the recommendation system
Now, I explored the various parameters of the *Item Based Collaborative Filter*. These parameters are default in nature. In the first step, k denotes the number of items for computing their similarities. Here, k is equal to 30. Therefore, the algorithm will now identify the k most similar items and store their number. 

### Exploring data science recommendation system model
Using the ```getModel()``` function, I retrieved the ```recommen_model```. I then found the class and dimensions of the similarity matrix, that is, contained within ```model_info```. Finally, I generated a heatmap, that will contain the top 20 items and visualize the similarity shared between them.

In the next step of the ML project, I carried out the sum of rows and columns with the similarity of the objects above 0. I visualized the sum of columns through a distribution.

### Building Recommender System on dataset using R
I created a ```top_recommendations``` variable which I initialized to 10, specifying the number of films to each user. I then used the ```predict()``` function that identified similar items and ranked them appropriately. Here, each rating is used as a weight. Each weight is multiplied with related similarities. Finally, I added everything in the end.

### Group Presentation Recording
[Group Presentation](https://drive.google.com/file/d/1bucUcJ60aItxyQOCtYAfnoIG9guIPuzb/view?usp=sharing)




📣  Feel free to have a look at all the files in this repository !🤗

#
### Languages used :
<code><img height="40" src="https://img.icons8.com/ios-filled/344/r.png"/></code>

#
❎ In case you find issues in any of my Repositories, you can Hit Me Up [here](https://github.com/Aditya-Bhate/Aditya-Bhate/issues)! 👈





