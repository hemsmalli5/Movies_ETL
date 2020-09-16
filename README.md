# Movies_ETL PipeLine
Through this challenge following objectives were achieved:
•	Created an automated ETL pipeline 
•	Extracted data from multiple sources
•	Cleaned and transformed the data using Pandas and regular expressions
•	Loaded new data into PostgreSQL database movies_data.

## Few Assumptions made while performing this task:
1. Here we try to assume that the Wikipedia data still contains imdb ids and try to catch them using try-catch block.
2. While merging we are assuming that dropping the redundant data (columns: 'title_wiki','release_date_wiki','Language','Production company(s)' ) wouldn’t loose good information.  
3. Assuming few missing data from Kaggle after the merge, missing kaggle data is addressed via file_missing_kaggle_data function.
4. As part of data extraction into DB, since the data file is large, assuming reading file in chucks of 1000000 will be better for data transfer 
5. As part of data extract, printing the elapsed time for final print would consider as a confirmation as data extract for each chunk and also provisioning chunk groups tracking
