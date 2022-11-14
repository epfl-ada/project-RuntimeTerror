# Building and analysis of movie arcs

Abstract (150 words): Most plots in the film business follow one of a few well-known story arcs. For example, consider a narrative in which the main character begins in turmoil and finishes in bliss, or in which the main character resides happily but has problems that he/she must overcome before returning to his/her joy. In this project, we propose to explore this phenomenon in order to identify the most common storylines, how profitable those storylines are, and the evolution of the most prevalent storyline with time.

Research question: 

Which correlations can be retrieved from movie arcs?
correlation between movie arcs and revenue? like does for example an action movie have a higher revenue, based on the dominantly negative plot? do people rather enjoy watching a movie with negative sentiments?


Additional datasets: ? which ones?, if yes how to get, manage, process and enrich them
Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible.

### Methods

found arc based on movie summary
We create story arcs by performing sentiment analysis on each line of the plot and determining the positivity/negativity of the relevant scene. We propose clustering movies based on the similarities of their story arcs constructed from the CMU Movie Summary Corpus dataset plots. -> 1st clustering by genres, take the top three movies from each genre

2nd clustering: cluster similar movies in each genre
-> depending on what? on the sentiments or on which category
1 idea: plot all movies of each genre and calculate mean, if mainly above/under mean, is it really a in this genre? 
2 idea: cluster by language, countries

With that, we can find the mean and variance of the revenue for each cluster, eventually leading to the identification of story arcs of the most profitable movie plots. Finally, we can repeat the same procedure but on a list of movie plots taken from different time frames hence resulting in a time series analysis of the evolution of the most prevalent story arcs.


added ratings from IMBd, matched with own dataset?
3 idea clustering: correlation of ratings with runtime? dominantly negative movie (like action) is better rated if long or short

### Proposed timeline
By 25.11.2022: 
By 02.12.2022: 
By 09.12.2022: 
By 16.12.2022: 
Deadline P3 submission: 23.12.2022


### Organization within team until P3
split by team members 


#### Questions for TA (if any)
