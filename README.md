# MOVIE-RECOMMENDATION-SYSTEM
My individual project titled movie recommendation system.
Content-Based-Movie-Recommender-System-with-sentiment-analysis-using-AJAX
Python Framework Frontend API

Updated version of this application can be found at: https://github.com/kishan0725/The-Movie-Cinema

Content Based Recommender System recommends movies similar to the movie user likes and analyses the sentiments on the reviews given by the user for that movie.

The details of the movies(title, genre, runtime, rating, poster, etc) are fetched using an API by TMDB, https://www.themoviedb.org/documentation/api, and using the IMDB id of the movie in the API, I did web scraping to get the reviews given by the user in the IMDB site using beautifulsoup4 and performed sentiment analysis on those reviews.

Check out the live demo: https://mrswsa.herokuapp.com/

Link to youtube demo: https://www.youtube.com/watch?v=dhVePtyECFw

Note
Use this URL - https://the-movie-buff.herokuapp.com/ - in case if you see application error in the above mentioned URL
The Movie Cinema
I've developed a similar application called "The Movie Cinema" which supports all language movies. But the only thing that differs from this application is that I've used the TMDB's recommendation engine in "The Movie Cinema". The recommendation part developed by me in this application doesn't support for multi-language movies as it consumes 200% of RAM (even after deploying it to Heroku) for generating Count Vectorizer matrix for all the 700,000+ movies in the TMDB.

Link to "The Movie Cinema" application: https://the-movie-cinema.herokuapp.com/

Don't worry if the movie that you are looking for is not auto-suggested. Just type the movie name and click on "enter". You will be good to go eventhough if you made some typo errors.

Source Code: https://github.com/kishan0725/The-Movie-Cinema

Featured in Krish's Live Session on YouTube
krish youtube

How to get the API key?
Create an account in https://www.themoviedb.org/, click on the API link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your API sidebar once your request is approved.

How to run the project?
Clone or download this repository to your local machine.
Install all the libraries mentioned in the requirements.txt file with the command pip install -r requirements.txt
Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
Replace YOUR_API_KEY in both the places (line no. 15 and 29) of static/recommend.js file and hit save.
Open your terminal/command prompt from your project directory and run the file main.py by executing the command python main.py.
Go to your browser and type http://127.0.0.1:5000/ in the address bar.
Hurray! That's it.
Architecture
IMG-20210306-WA0012

Similarity Score :
How does it decide which item is most similar to the item user likes? Here we use the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

image

More about Cosine Similarity : Understanding the Math behind Cosine Similarity

Sources of the datasets
IMDB 5000 Movie Dataset
The Movies Dataset
List of movies in 2018
List of movies in 2019
List of movies in 2020
