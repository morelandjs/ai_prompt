# ai_prompt
Automated Insights programming evaluation

Requires python3 and python libraries matplotlib, numpy, and stop_words.
The python libraries can be installed with pip, e.g.,

`pip3 install matplotlib numpy stop_words`

This script reads 'movie_data.csv' which is expected in the current working directory.
The dataset can be downloaded by visiting [dropbox](https://www.dropbox.com/s/ge8dsb56vv9ofd4/movie_data.csv).

The purpose of this script is to analyze the file 'movie_data.csv' and answer several simple questions:

- First, the script aggregates the complete list of movie genres and determines which genres are the most popular.
It prints the five most popular genres to std out.

- Second, it loops through these five most popular genres and collects the movie summary text for all movies associated with that genre.
The most common words are then counted in each genre and the script prints the information to std out.

- Third, the script tests the strength of [Zipf's law](https://en.wikipedia.org/wiki/Zipf's_law) for the distribution of word frequencies in text corpora.
This is achieved by scatter plotting word rank (least to most common) vs frequency (number of occurences) using the available movie summary data.
The data is finally compared to a linear fit on a log-log scale and the comparison figure is saved to a pdf.
