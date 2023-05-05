# Creole Linguistics Analysis

This project analyzes the use of Patois (Jamaican Creole) in Jamaican music lyrics over time. The analysis involves data cleaning, word counting, and data visualization.

## Data

The project uses three datasets:

- `english_words.txt`: a list of 466,589 English words that are found in the Oxford Dictionary 
- `english_words_patois_edit.txt`: And edit of english_words.txt to remove words that are patois words which are used differently in patois*
- `lyrics_Final.xlsx`: a dataset of song lyrics from various Jamaican artists. I created this dataset by making a Python script that extracts the lyrics of Jamaican songs from the Genius API, given the artist                          and song name, and saves them to an Excel file which was then imported into R studio 

## Data Cleaning

-The project cleans the lyrics by removing any words ending with "embed" from the Lyrics column. 
-The project converts all the words in the Lyrics Column to lowercase to improve the accuracy of word detection.

## Data Analysis

The project analyzes the data by counting the number of English and Patois words in each song. It then calculates the percentage of Patois words and English words in each song.
To do this , the code calculates the number of English words and Patois (Jamaican Creole) words in each row of the dataset lyrics_final and stores the counts in two variables english_word_count and patois_word_count.The code then creates a data frame word_counts with six columns: Artist, Song, Year, Genre, English Words, and Patois Words. The code uses a for loop which iterates through each row of lyrics_final and uses the strsplit() function to split the lyrics of each song into individual words. For each word, the program checks if it is present in the english_words_patois_edit.txt file. If it is, the word is stored in the list of English words, and if not, it is stored in the list of Patois words. The program then counts the number of English and non-English words and stores them in the english_word_count and patois_word_count lists, respectively.  

Finally, the code creates a new data frame word_counts that combines the columns of lyrics_final with the English Words and Patois Words counts for each song. The column names are then assigned to the appropriate labels. This data frame can then be used for further analysis, such as generating plots or calculating statistics on the language use in Jamaican music.

## Data Visualization

The project visualizes the data in two ways (Work in Progress):

### Bar Chart of Patois Percentage for Dancehall Songs

The project creates a bar chart that shows the percentage of Patois words in each Dancehall song. The chart is sorted in ascending order by year, and each bar is labeled with the song name.

### Stacked Bar Chart of English and Patois Word Counts

The project creates a stacked bar chart that shows the total number of words in each year. The bars are split into English and Patois words, showing the proportion of each in each year.

## Conclusion

This project provides insights into the use of Patois in Jamaican music lyrics over time. The data suggests that Patois usage has increased over the years, particularly in the Dancehall genre.
