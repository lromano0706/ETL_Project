# ETL_Project
Taking Video Game Data Set from Kaggle and Combining it with Publisher Data set

Extract:
  We decided to use a csv dataset found on kaggle containing information on videogame sales and scraped videogame publisher information from wikipedia. At first we wanted to use developer information but we realized that developers often had many company names and that would be difficult to handle so we switched over to publishers.
  
Transform:
  We converted the data into pandas dataframes and removed any unnecessary columns. We made sure that the publisher names of both datasets had identical formatting by converting the names of uppercase. We then removed special characters from column names because mongo would not accept them. We also removed null values from the datasets.
  
Load:
  We decided to use mongo because most records did not have complete information but we did not want to have too many null values. The database is named videogames_db and it contains one collection: games. The games collection can contain the following fields if the information exists: Sales Rank, Name, Genre, ESRB Rating, Platform, Publisher, Developer, Critic Score, User Score, Total Shipped, Global Sales, NA Sales, PAL Sales, JP Sales, Other Sales, Year, Publisher location, Publisher Established Date.
