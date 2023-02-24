# Final_Project: Movie Analysis
## First Project Segment

### Overview:

####    Most of America and worldwide households have heard of IMBD, a database created to provide information and rating about the movie we enjoy watching. Today we want to bring you information about FilmTV an Italian movie rating database that further brakes down these rating using subcategories that provide us with a more in depth understanding of each movie. Movies are watched all over the world by so many, they can be found not only playing in households but also in businesses and schools alike. These films have several purposes and are used for many reasons, sometimes being watched for simple entertainment, for learning & teaching, to pass time or a reason to spend quality time with loved ones. Databases like FilmTV and IMBD allow its visitors to explore information about a movie’s casting, summaries, fan favorites, critic reviews and of course ratings. FilmTV goes a step further by using sub rating categories that tell us if a movie is erotic, humors, the tension, rhythm and effort. We used these subcategories and other features to further break down not only how people feel about movies via their ratings but how these other factors also have an impact on those same ratings. 

####    The data set we used for this project was found on Kaggle.com, it provided over 40,000 data points from the FilmTV database, allowing us to analyze how different variables can impact ratings. This data set includes several details of each movie including movie length, name, genre, names of actors, names of directors, country the movie was created, average vote, critic vote, and scores on how humorous the movies were, as well as other indicators. As a group we decided to create machine learning models that can accurately predict which feature can contribute to a high average rating for these movies.

####    Now that we know our dataset, we needed to minimize and remove some of the columns we deemed irrelevant for our use with this project. This also allowed us to shrink down the data enough to be uploaded to GitHub and to be cleaned. For this project we decided to use Jupyter Notebook to show our work and to use Tableau to create the visualizations. We will also use CSV’s to upload our cleaned and updated data into.

### Roles:

#### Kristina: Tasked with creating the readme and creating a Randome Forest model.Once the dataset was clean, I focused on deciding which columns needed to be dropped or processed numerically. Once that was done, I created an initial random forest model. One of the models used only five feature which were erotism, tension, humor, effort, and rhythm with the target value of avg_vote greater than or equal to 7. The features used in this model represent a score each movies based on how much effort, rhythm and so on the movie is thought to have. This produced an acccuracy of 79%. For my next attempt at creating a more accurate random forest model I added more variables. The variables I added included countries, actors, duration, year, total_votes, critic_votes, and genre. With the genre and actors columns some adjustments needed to be made in order to put their values in a numerical format create a successful machine learning model. Once that was done I was able to create the model and received a 96% accuracy.  

#### Karina: Tasked with creating a Logistic Regression model and aiding in the creation/modifying google slides. I used the cleaned tvfilm csv file to create a Logistic Regression model for several variables and compared it to the target (avg_vote). I used the different samplings (over/under/combination) and found that random oversampling was the best for the dataset due to yielding the highest balanced accuracy score. I tested four different variables:

##### Model 1: Duration
<img width="710" alt="Screenshot 2023-02-17 at 2 53 12 PM" src="https://user-images.githubusercontent.com/110318652/219778931-72c727c0-4e1e-4431-b526-5f0df09a8086.png">

#### The avg_vote column was the target variable and I created a threshold of 7.0, meaning anything under would be considered unpopular. I also created a new column comparing the films popularity, zero meaning unpopular and one meaning popular. I set the X value as the duration column.

<img width="473" alt="Screenshot 2023-02-17 at 2 53 59 PM" src="https://user-images.githubusercontent.com/110318652/219778929-98eef7b8-5a74-4b2d-bd2c-9447f8832455.png">

#### As shown above, the balanced accuracy score yields to 56.8%.

##### Model 2: Tension
<img width="472" alt="Screenshot 2023-02-17 at 3 05 33 PM" src="https://user-images.githubusercontent.com/110318652/219783245-baaa8f04-e5e9-4d70-983b-2f6e140bdd14.png">

#### For this model, I set tension as my X variable. I yielded a balanced accuracy rate of 65.8%.

##### Model 3: Humor, Rhythm, Effort, Tension, Erotism
<img width="476" alt="Screenshot 2023-02-17 at 3 06 13 PM" src="https://user-images.githubusercontent.com/110318652/219783243-4db26336-318e-4980-b272-c6e0a1e5b253.png">

#### The humor, rhythm, effort, tension, and erotism were tested in this model. The balanced accuracy rate was 70.1%.

##### Model 4: Humor, Rhythm, Effort, Tension, Erotism, Year, Duration, Country, Genre, Top Actor
<img width="471" alt="Screenshot 2023-02-17 at 3 13 04 PM" src="https://user-images.githubusercontent.com/110318652/219784092-aac2e58b-de64-47bc-925c-5b48feb65a95.png">

#### I added from the release year of the film/tv, its duration, the top 5 countries of release, top 5 genre, and the top actors from model 3. It yielded the highest balanced accuracy rate of 73.4%.

##### Conclusion:
#### As stated, this further fits the narrative that films and tv series are complex. There are various elements that play a role in yielding a high accuracy score. Film and TV series are rated by their descriptive elements rather the genre. We clearly see in the first model, duration alone was not enough to yield a high score. Model 2 did yield higher but not as high as the added elements on model 3. Model 4 had the most descriptive elements and yielded the highest balanced accuracy score.


#### Group: Undecided specifics of visualization work.
#### Dillon: Tasked with the initial cleaning of the data set and creating a Linear Regression model. Initially with my dataset, I wanted to see if a linear regression model might be able to show a correlation between the genre of a film and the average score the audience rated the film. Naturally, I ran the machine learning model and received a little to no correlation between average vote and genre. In our dataset, there are several other columns such as tension, rhythm, erotism, etc. Determining how these features are determined is not told to us by the Kaggle data-set page, so I am investigating how these numbers come about. Leaving that aside for now, when I split the data to see if the popular films, where the average score was greater than 7 out of 10, correlated with eoritsm, rhythm, effort, my linear regression model yielded an r-squared of 81%. After investigating to more into the tension, rhythm, erotism, effort, and humor features I discovered a couple of things. IMDB simply offers an overall score of a film not including features like effort, rhythm, erotism, etc. On the other hand, our dataset stems from an Italisn movie rating website, called filmtv.it, where they give an overall rating of a film, similar to that of IMDB, as well as a rating from 1-5 rating the tension, rhythm, erotism, effort, and humor of the film. With respect to the machine learning aspect of the project, my group chose my machine learning model as our main model. I've switched from my linear regression model to a Random Forest in order to better highlight the complex comparisons of my data. In using the Random Forest model I was able to produce 3 models that help tell our story. 

#### Model 1


![model 1 final project ](https://user-images.githubusercontent.com/112899813/219524629-377f11ef-3a6e-49a0-9cad-5892910c87f4.png)


#### As you can see in the model above, my X values are year (The year the film was released), the duration (the length of the film), country_grouped (the top 5 countries that pump out films each year), genre_grouped (the top 5 genres), and has_top_actors (the top 100 actors). My y value in the model is popular (popular here indicates where the average vote is greater than 7 out of 10). After running the model I got an r-squared of 78%. 


#### Model 2


![model 2 final project ](https://user-images.githubusercontent.com/112899813/219528005-2667c662-c48c-4346-83e1-028c5796bb43.png)


#### My second model, which really pertains to our research project more objectively, shows the features tension, rhythm, erotism, effort, and humor compared to the previous y value: popular. This model offered an r-squared of 81% which is a bit higher than our previous model. 


#### Model 3


![Model 3 final project ](https://user-images.githubusercontent.com/112899813/219529124-ccdc2819-d84f-4682-a120-a2addc1b269b.png)


#### My final model essentially groups all of the previous variables as the X and compares them all to our typical y value: popular. This model offered the highest r-squared with an 82%. 

#### Summary 

#### The second machine learning model, which focuses on the tension, rhythm, erotism, effort, and humor features show that these elements play a larger role in yielding a higher r-squared when compared to genre, year, top countries, etc. This fits with our new research idea, which is movies are very complex and a lot of various elements play a role in yielding strong correlation with respect to the films average score. Initially we wanted to try and find a correlation between the average vote of a film and genre. After figuring out that this offered little to no correlation, we discovered that the tension, rhythm, erotism, effort, and humor features play a much larger role in people's liking of a film. The conclusion we have is that a film's rating, no matter the genre, depends more upon various descriptive elements. A film that is categorized as a comedy can score badly if the humor feature is rated low in the film. A more complex film, that has, let's say a high rating for all of the descriptive features, is more likely to have an overall higher film score as opposed to one that does not. The third model provided simply shows all of the descriptive features plus the other variables, shows that as you add complexitiy to the machine learning model, it will yield a higher r-squared. 


### Visualizations 
#### CC's role: Editing our readme and creating visualizations that correlate with the team’s data. Created visualizations that showed how a movie’s duration can have an impact of ratings/votes. Movies that are “too short” had fewer ratings, however movies with longer durations had more votes/popularity. It was also found that specific genres change the impact of the subcategories, example; comedy was found to have higher results for humor and rhythm where as horror had lest humor and more tension.

#### One of the questions my group tried to answer during this project was if a movie’s duration could have an impact on voting. I found that most of the votes received are for movies within 30 minutes to 2 hours. The duration didn’t specifically impact on the number of votes I did find that moves with longer duration had a tendency to receive higher votes. 
![project image one](https://user-images.githubusercontent.com/112769590/220768863-a6a3908b-b0d8-4c3a-9184-e8f8608090d3.png)

#### The following image shows how the 5 sub voting categories found within each genre can have an impact on the vote. 
![project image two](https://user-images.githubusercontent.com/112769590/220769428-b9b221b6-2426-4038-8b92-a641642208e7.png)


#### To interact with the visualizations captured please follow this link
https://public.tableau.com/app/profile/comaneci.christie/viz/FinalProject_16765076708500/finalproject?publish=yes

