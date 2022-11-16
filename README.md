# Building and analysis of movie arcs

Abstract (150 words): 

Research question: 

Which correlations can be retrieved from movie arcs?
correlation between movie arcs and revenue? like does for example an action movie have a higher revenue, based on the dominantly negative plot? do people rather enjoy watching a movie with negative sentiments?


Additional datasets: ? which ones?, if yes how to get, manage, process and enrich them
Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible.

### Methods

found arc based on movie summary
Most plots in the film business follow one of a few well-known story arcs. For example, consider a narrative in which the main character begins in turmoil and finishes in bliss, or in which the main character resides happily but has problems that he/she must overcome before returning to his/her joy. In this project, we propose to explore this phenomenon in order to identify the most common storylines, how profitable those storylines are, and the evolution of the most prevalent storyline with time.
We create story arcs by performing sentiment analysis on each line of the plot and determining the positivity/negativity of the relevant scene. We propose clustering movies based on the similarities of their story arcs constructed from the CMU Movie Summary Corpus dataset plots. -> 1st clustering by genres, take the top three movies from each genre

Split into Part one and two
Part one: mainly getting familiar with the data and constructing story arcs. For this the plot summaries have been read into as id and plot of each movie. Plot split into sentences as array. Build sentiment analyzer with vader sentiment as sentiment instensity analyzer, which gives back a continuous sentiment score. Additionally this score has been classified into positive (1), neutral (0) and negative (-1) scores. To add more information in the dataframe, the plot summaries with the sentiment scores were merged with the movie metadata dataset, which added the release date, title, box office sales, production country and genre. Because we are interested in the revenue depending on the movie genre, the new dataset has been processed by removing all movies without revenue values. (reduced dataset to a sixth of the initial)
The next step it so split the data into their genres. all genres are sectioned in the four most common genres: adventure, action, drama and comedy. (do need to add which genres in which main genre?)
columns = zip_longest(*list_values, fillvalue=0) what does * mean?

For every main genre, the most common movie arc was retrieved, by taking the average of all datapoints? And plotting them. In addition, all four genres were clustered depending on their movie arc in three clusters. How? What is 
gak_km = KernelKMeans(n_clusters=3, kernel="gak")


To further analyze our data, the second part processed the data to undertake different comparisons. Here, each movie was divided into either a positive movie, negative movie or neutral movie, depending on the sentiment plot classification. The movie is classified in to a positive movie if 70% percent of the overall sentiment scores are positive scores (+1). Same approach was used for the negative movies. The rest is classified as a neutral movie.

An additional data set was used, the ratings from ???, where only the data regarding movies was used (no other category). It contains the average rating, its number of votes and the title. 
??? -> was it later merged with the other df like the movie plots etc?

1 idea: plot all movies of each genre and calculate mean, if mainly above/under mean, is it really a in this genre? 

With that, we can find the mean and variance of the revenue for each cluster, eventually leading to the identification of story arcs of the most profitable movie plots. Finally, we can repeat the same procedure but on a list of movie plots taken from different time frames hence resulting in a time series analysis of the evolution of the most prevalent story arcs.


added ratings from IMBd, matched with own dataset?
3 idea clustering: correlation of ratings with runtime? dominantly negative movie (like action) is better rated if long or short

### Proposed timeline
For the final milestone, you will be expected to execute your project proposal and describe your project in a data story. Data stories are a blog post or short article, with an important visual component, using data to tell a story and illustrate it effectively. You can be less formal here (although methods and math should then appear in the notebook), but more visual.

By 09.12.2022: get familiar with Jekyll (to build website)
By 16.12.2022: statisitical analysis
Deadline P3 submission: 23.12.2022 finalize website, finalize single notebook, update readme (with details of contributions)


### Organization within team until P3
split by team members 


#### Questions for TA (if any)

