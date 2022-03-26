**LAB 1 - Oleskevych Sofia, CS-314**


---

1.Install venv
```
python -m venv .VENV
.VENV\Scripts\activate
```
2.Install requirements
```
pip install -r requirements.txt
```
3.Run main.py

4.[Google colab](https://colab.research.google.com/drive/13baGetSPnSxeS77hDKtpZVb-S3ehjkH7#scrollTo=srvM8D6nRdJA)

_for comfortable view run it:)_



---
TASK DESCRIPTION
---



***Analysis part***

I loaded “movies_metadata.csv” and ”ratings.csv” (or ratings_small.csv) as spark dataframes https://www.kaggle.com/rounakbanik/the-movies-dataset/data

Saved them to Google Drive, mounted GD to my colab notebook.

Using Python + Pyspark performed basic investigation and printed out summary (are there any missing values; How many records; How many unique users are there)


---


***Preprocessing part***

Using pyspark DataFrame API transform data loaded on a previous step to create MovieProfile and UserProfile entities with following schemas: 


---


**MovieProfile entity schema**:

•	MovieId - id of the movie

•	MovieName - name of the movie

•	MovieRating - average from all the user ratings for the movie

•	Genres - a string with the comma separated genres for the movie



---



**UserProfile entity schema**:

•	UserId - id of the user

•	NumberOfMarks - how many marks user left

•	YearsSpent - how many years has passed since the first mark

•	AvgMark - average user mark

•	AvgTimeBetweenMarks - how often user watches movies - how many time in average user spends between the marks in days (if I have 3 marks on the next dates: 21.07, 23.07 and 27.07, I will have (2 + 4) / 2 = 3 days in average)

•	FavoriteGenre - favorite genre of a user (my own implementation)



