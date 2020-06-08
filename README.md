# Topic modelling 
In this project we try to find topics using Latent Dirichlet Allocation in the songs lyrics.

## Data
The was originally taken from Kaggle, which you can find [here](https://www.kaggle.com/gyani95/380000-lyrics-from-metrolyrics).

The dataset consists of more than 380 000 observations, each observation shows name of the song, release year, artist, genre and lyrics of the song themself. We are mostly interested in ‘lyrics’ and ‘genre’ information. The original dataset presented the following genres: ['Pop', 'Hip-Hop', 'Not Available', 'Other', 'Rock', 'Metal', 'Country', 'Jazz', 'Electronic', 'Folk', 'R&B', 'Indie']. We decided to exclude ‘Not Available’ and ‘Other’ categories from the sample as we think there is no special semantic or featured vocabulary, which might statistical methods could analyse.

![GitHub Logo](/images/distribution.jpeg)

Around 45% of all lyrics that are represented as ‘Rock’ music, the second largest group is ‘Pop’ music with 17% of the sample. The smallest group in the sample is ‘Folk’ music, it represents around 1% of the sample.

## Topic Modelling
Cleaning the data for this task is performed in the 'data_cleaning_topic.ipynb' file. 

We implemented the Latent Dirichlet Allocation (LDA) for this dataset. See [here](http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf). 

LDA finds topics in the dataset in unsupervised manner. We can then return the 'key words' of each topic in the dataset.
![GitHub Logo](/images/results1.jpeg)

The first thing that we think is really interesting in this output, that you can actually able to guess the genre in the output. For example: row 0 is apparently ‘Metal’, row 1 could be ‘Folk’,and we could also find some other genres in the output. Interesting thing in terms of the results, that was provided by the method, that it actually identified languages as a separate topics in the data (we can try to call them ‘German’ and ‘Spanish’ genres in out setup). This is how we identified that the dataset has lyrics in languages, other than English. So, we had to return to the cleaning part again to get rid of the 30 000 songs more.

In order to identify the language, we used langdetect python’s package.

As we cleaned the data, we updated the results of the LDA.

![GitHub Logo](/images/results2.jpeg)

We think that genres could be identified as follows:
0: Indie, 1: Rock, 2: R&B, 3: Jazz, 4: Electronic, 5: Country, 6: Metal, 7: Pop, 8: Hip-Hop, 9: Folk.

LDA gives supring results! Most of the words intuitively suggest us the genre represented by the words. Though as some genres like Hip-Hop and R&B, Folk and Indie may be hard to identify as they might use similar vocabulary in their ‘Topics’.
