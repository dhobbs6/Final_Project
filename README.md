# Final_Project: Movie Analysis
## First Project Segment

### Overview:

####    When we initially received our final project requirement, our team went through several different data set topics in an effort to find information that not only worked for our project but was also exciting. And what is more exciting than movies! Movies are watched by people fom all over the world, by the young, by families, for learning purposes, for romance, to pass time, for entertainment and to simply spend quality time with loved ones. Most people that watch movies have an opinion about what they have watched whether good or bad. As a result, databases like IMDB were created to provide information about those movies. Some of the information that can be found in an IMDB database is a movie’s casting information, summaries, fan reviews, critic reviews, trivia, and ratings.

####    For our project we found a data set on Kaggle.com that had over 40,000 data points from the IMDB database that we used to analyze how different variables can impact ratings. This data set includes several details of each movie including movie length, name, genre, names of actors, names of directors, country the movie was created, average vote, critic vote, and scores on how humorous the movies were, as well as other indicators. As a group we decided to create machine learning models that can accurately predict which feature can contribute to a high average rating for these movies.

####    Now that we know our dataset, we needed to minimize and remove some of the columns we deemed irrelevant for our use with this project. This also allowed us to shrink down the data enough to be uploaded to GitHub and to be cleaned. For this project we decided to use Jupyter Notebook to show our work and to use Tableau to create the visualizations. We will also use CSV’s to upload our cleaned and updated data into.

### Roles:

#### Kristina: Tasked with creating the readme and creating a Randome Forest model.Once the dataset was clean, I focused on deciding which columns needed to be dropped or processed numerically. Once that was done, I created an initial random forest model. One of the models used only five feature which were erotism, tension, humor, effort, and rhythm with the target value of avg_vote greater than or equal to 7. The features used in this model represent a score each movies based on how much effort, rhythm and so on the movie is thought to have. This produced an acccuracy of 79%. For my next attempt at creating a more accurate random forest model I added more variables. The variables I added included countries, actors, duration, year, total_votes, critic_votes, and genre. With the genre and actors columns some adjustments needed to be made in order to put their values in a numerical format create a successful machine learning model. Once that was done I was able to create the model and received a 96% accuracy. 
#### CC: Visualization work and readme editing.

#### Karina: Tasked with creating a Logistic Regression model, and aid in creating/modifying powerpoint. I used the cleaned tvfilm csv file to create a logistic regression model for several variables. Used the different approaches (over/under/combination sampling) and found that random oversampling was the best for the dataset due to yielding the highest balanced accuracy score. I initially started with duration and avg_votes, yielding a 56.8% balanced accuracy score. I then tried tension, making the score 65.8%. I then added more variables (humor, rhythm, effort, tension, erotism) and yielding a balanced accuracy score of 70.1%. When I added year, duration, country, genre, and top actors to my X variable, yielding a 73.1%. 
<img width="473" alt="Attempt 4" src="https://user-images.githubusercontent.com/110318652/219529067-bd8aeb50-1c51-44e1-bd7c-31727c80c5cd.png">


#### Group: Undecided specifics of visualization work.
#### Dillon: Tasked with the initial cleaning of the data set and creating a Linear Regression model. Initially with my dataset, I wanted to see if a linear regression model might be able to show a correlation between the genre of a film and the average score the audience rated the film. Naturally, I ran the machine learning model and received a little to no correlation between average vote and genre. In our dataset, there are several other columns such as tension, rhythm, erotism, etc. Determining how these features are determined is not told to us by the Kaggle data-set page, so I am investigating how these numbers come about. Leaving that aside for now, when I split the data to see if the popular films, where the average score was greater than 7 out of 10, correlated with eoritsm, rhythm, effort, my linear regression model yielded an r-squared of 81%. 


### Google Sheets
https://docs.google.com/presentation/d/1AR3GUSF049e1tsglMIXLhkLZ1TvVr6j2IbQkQhFHbmE/edit?userstoinvite=kris91398%40gmail.com&actionButton=1#slide=id.g2086a904554_0_29
