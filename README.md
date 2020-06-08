# Metal lyrics generator 
In this project we implemented 2 methods that are common in natural language processing: topic modelling and text generation for the lyrics data. 

## Data
The was originally taken from https://www.kaggle.com/gyani95/380000-lyrics-from-metrolyrics. 

The dataset consists of more than 380 000 observations, each observation shows name of the song, release year, artist, genre and lyrics of the song themself. We are mostly interested in ‘lyrics’ and ‘genre’ information. The original dataset presented the following genres: ['Pop', 'Hip-Hop', 'Not Available', 'Other', 'Rock', 'Metal', 'Country', 'Jazz', 'Electronic', 'Folk', 'R&B', 'Indie']. We decided to exclude ‘Not Available’ and ‘Other’ categories from the sample as we think there is no special semantic or featured vocabulary, which might statistical methods could analyse.

