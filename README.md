# Weekend-Movie-Trip

This project focuses on a movie dataset with the inclusion of the movie title, ratings and genres of each of the movies included. The goal of this project is to provide an appropriate visual representation to predict favorable movies for users based on the ratings and genres of the movies.

The contents of this repo are this ReadMe file, a folder with the data sets that I used and my JuPyter notebook file.

In order to provide an accurate reading of the genres, I needed to onehot encode the genres, so i had to make a set of all of the genres included (which was available in the 'genres' column) and make one column for each individual genre. I then detected if the 'genres' column for each row contained one of the genres and filled the corresponding column with a 1. All other unfilled spaces were assigned a 0. Another bit of feature engineering that I used was the year the movie came out. I used a string command to get the string values between -1 and -6 to get the year the movie came out. 

The models that I planned to use were k-means and mean shift. To decide the number of clusters to use for k-means, I used an elbow analysis to find the proper number of clusters (which was 3) to fit my dataset. For my attempt at mean shift, I used the function sk.estimate_bandwidth for an estimation of the aproxximation window to calculate the initial mean values.

Overall, my results were not indicative of any significant trend, since the feature engineering that I performed did not link the genres and yearly release of the movie to their ratings. If I could have done things a bit differently with the feature engineering, then I would have found some way to better link the movies to the individual users instead of trying to link the movie ratings to their genres.

My K-means analysis did not reveal any significant-looking clusters, as two of the three clusters seemed to dominate the dataset. Unfortuneately, I was unable to obtain proper analysis of my mean shift method due to long computational times. My method of bypassing this if I had more time would be to lower the number of iterations or sample a smaller set of data, since there were so many closely oriented data points.
