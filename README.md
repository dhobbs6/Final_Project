# Final_Project: Movie Genre Analysis
## First Project Segment

### Overview:

####    When we initially received our final project requirement, our team went through several different data set topics in an effort to find information that not only worked for our project but was also exciting. And what is more exciting than movies! Movies are watched by people fom all over the world, by the young, by families, for learning purposes, for romance, to pass time, for entertainment and to simply spend quality time with loved ones. Most people that watch movies have an opinion about what they have watched whether good or bad. As a result, databases like IMDB were created to provide information about those movies. Some of the information that can be found in an IMDB database is a movie’s casting information, summaries, fan reviews, critic reviews, trivia, and ratings.

####    For our project we found a data set on Kaggle.com that had over 40,000 data points from the IMDB database that we used to analyze how different variables can impact ratings. This data set includes several details of each movie including movie length, name, genre, names of actors, names of directors, country the movie was created, average vote, critic vote, and scores on how humorous the movies were, as well as other indicators. As a group we decided to create machine learning models that can accurately predict which feature can contribute to a high average rating for these movies.

####    Now that we know our dataset, we needed to minimize and remove some of the columns we deemed irrelevant for our use with this project. This also allowed us to shrink down the data enough to be uploaded to GitHub and to be cleaned. For this project we decided to use Jupyter Notebook to show our work and to use Tableau to create the visualizations. We will also use CSV’s to upload our cleaned and updated data into.

### Roles:

#### Kristina: Tasked with creating the readme and creating a Randome Forest model.
#### CC: Visualization work and readme.
#### Karina: Tasked with creating a Logistic Regression model.
#### Dillon: Tasked with the initial cleaning of the data set and creating a Linear Regression model. Initially with my dataset, I wanted to see if a linear regression model might be able to show a correlation between the genre of a film and the average score the audience rated the film. Naturally I ran the machine learning model and received a little to no correlation between average vote and genre. In our dataset, there are several other columns such as tension, rhythm, erotism, etc. I was curious about these various columns and what they mean. When splitting the data and seeing if the popular films, where the average score was greater than 7 out of 10, correlated with eoritsm, rhythm, effort, my linear regression model yielded an r-squared of 81%. 


