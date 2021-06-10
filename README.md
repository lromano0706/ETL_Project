# ETL_Project
Taking Video Game Data Set from Kaggle and Combining it with Developer Data set

Extract:
  We decided to use a csv dataset found on kaggle containing information on videogame sales and scraped videogame publisher information from wikipedia. At first we wanted to use developer information but we realized that developers often had many company names and that would be difficult to handle so we switched over to publishers.
  
Transform:
  We converted the data into pandas dataframes and removed any unnecessary columns. We made sure that the publisher names of both datasets had identical formatting by converting the names of uppercase. We then removed special characters from column names because mongo would not accept them.
  
Load:
  We decided to use mongo because we wanted the option to add the videogame artwork to the database. The database is named videogames_db and it contains two collections: games and publishers.
