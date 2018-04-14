# Netflix_movie_recommendation_system
This project aims to build a movie recommendation system with Netflix dataset I used here come directly from Netflix. It consists of 4 text data files, each file contains over 20M rows, i.e. over 4K movies and 400K customers. All together over 17K movies and 500K+ customers!
One of the major challenges is to get all these data loaded into the Kernel for analysis, I have encountered many times of Kernel running out of memory and tried many different ways of how to do it more efficiently.

### Content
This comes directly from the README

### TRAINING DATASET FILE DESCRIPTION
The file "training_set.tar" is a tar of a directory containing 17770 files, one per movie. The first line of each file contains the movie id followed by a colon. Each subsequent line in the file corresponds to a rating from a customer and its date in the following format:

CustomerID,Rating,Date

MovieIDs range from 1 to 17770 sequentially.
CustomerIDs range from 1 to 2649429, with gaps. There are 480189 users.
Ratings are on a five star (integral) scale from 1 to 5.
Dates have the format YYYY-MM-DD.

### MOVIES FILE DESCRIPTION
Movie information in "movie_titles.txt" is in the following format:

MovieID,YearOfRelease,Title

MovieID do not correspond to actual Netflix movie ids or IMDB movie ids.
YearOfRelease can range from 1890 to 2005 and may correspond to the release of corresponding DVD, not necessarily its theaterical release.
Title is the Netflix movie title and may not correspond to titles used on other sites. Titles are in English.

### QUALIFYING AND PREDICTION DATASET FILE DESCRIPTION
The qualifying dataset for the Netflix Prize is contained in the text file "qualifying.txt". It consists of lines indicating a movie id, followed by a colon, and then customer ids and rating dates, one per line for that movie id. The movie and customer ids are contained in the training set. Of course the ratings are withheld. There are no empty lines in the file.

MovieID1:

CustomerID11,Date11

CustomerID12,Date12

...

MovieID2:

CustomerID21,Date21

CustomerID22,Date22

For the Netflix Prize, your program must predict the all ratings the customers gave the movies in the qualifying dataset based on the information in the training dataset.

The format of your submitted prediction file follows the movie and customer id, date order of the qualifying dataset. However, your predicted rating takes the place of the corresponding customer id (and date), one per line.

For example, if the qualifying dataset looked like:

111:

3245,2005-12-19

5666,2005-12-23

6789,2005-03-14

225:

1234,2005-05-26

3456,2005-11-07

then a prediction file should look something like:

111:

3.0

3.4

4.0

225:

1.0

2.0

which predicts that customer 3245 would have rated movie 111 3.0 stars on the 19th of Decemeber, 2005, that customer 5666 would have rated it slightly higher at 3.4 stars on the 23rd of Decemeber, 2005, etc.

You must make predictions for all customers for all movies in the qualifying dataset.

### THE PROBE DATASET FILE DESCRIPTION
To allow you to test your system before you submit a prediction set based on the qualifying dataset, we have provided a probe dataset in the file "probe.txt". This text file contains lines indicating a movie id, followed by a colon, and then customer ids, one per line for that movie id.

MovieID1:

CustomerID11

CustomerID12

...

MovieID2:

CustomerID21

CustomerID22

Like the qualifying dataset, the movie and customer id pairs are contained in the training set. However, unlike the qualifying dataset, the ratings (and dates) for each pair are contained in the training dataset.

If you wish, you may calculate the RMSE of your predictions against those ratings and compare your RMSE against the Cinematch RMSE on the same data. See http://www.netflixprize.com/faq#probe for that value.

### Acknowledgements
The training data came in 17,000+ files. In the interest of keeping files together and file sizes as low as possible, I combined them into four text files: combined_data_(1,2,3,4).txt

The contest was originally hosted at http://netflixprize.com/index.html

The dataset was downloaded from https://archive.org/download/nf_prize_dataset.tar

### Inspiration
This is a fun dataset to work with. You can read about the winning algorithm by BellKor's Pragmatic Chaos here