# Project_2_Team_4
Team 4 challenged ourselves to each complete the full mini-project, and then come together to understand how (and if) we solved things differently.  
We’ve each included our python file, ERD image, and sql db file in our git repository, as well as an aggregated version of our solutions.  

Team 4:  
Kathryn McAtee  
Sam Smith  
Deidre Lebron  
Fran Ruiz  

# Extracting the Data  
After importing the necessary libraries defined in the ipynb, we extracted the data from the crowdfunding.xls with a plan to create 4 dataframes before creating an ERD and SQL database.

# Creating 4 DataFrames:  

# 1. Category DF  
Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:  
• A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories  
• A "category" column that contains only the category title  
• Export the category DataFrame as category.csv and save it to your GitHub repository.  

# 2. Sub-Category DF  
Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:  
• A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories  
• A "subcategory" column that contains only the subcategory titles  
• Export the category DataFrame as subcategory.csv and save it to your GitHub repository.  

# 3. Campaign DF  
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:  
• The "cf_id" column  
• The "contact_id" column  
• The "company_name" column  
• The "blurb" column, renamed to "description"  
• The "goal" column, converted to the float data type  
• The "pledged" column, converted to the float data type  
• The "outcome" column  
• The "backers_count" column  
• The "country" column  
• The "currency" column  
• The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format  
• The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format  
• The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame  
• The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame  
• Export the category DataFrame as campaign.csv and save it to your GitHub repository.  

# 4. Contacts DF  
Team 4 chose to solve the problem both ways:  
• Option 1: Use Python dictionary methods.  
• Option 2: Use regular expressions.  

We followed the following steps for Option 1:  
• Import the contacts.xlsx file into a DataFrame.  
• Iterate through the DataFrame, converting each row to a dictionary.  
• Iterate through each dictionary, doing the following:  
• Extract the dictionary values from the keys by using a Python list comprehension.  
• Add the values for each row to a new list.  
• Create a new DataFrame that contains the extracted data.  
• Split each "name" column value into a first and last name, and place each in a new column.  
• Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.  

We followed the following steps for Option 2 and captured multiple ways of solving the problem via Regex:  
• Import the contacts.xlsx file into a DataFrame.  
• Extract the "contact_id", "name", and "email" columns by using regular expressions.  
• Create a new DataFrame with the extracted data.  
• Convert the "contact_id" column to the integer type.  
• Split each "name" column value into a first and a last name, and place each in a new column.  
• Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.  

# Creating the Crowdfunding Database  
• Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site.    
• Use the information from the ERD to create a table schema for each CSV file.  
Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.   
• Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.  
• Create a new Postgres database, named crowdfunding_db.  
• Using the database schema, create the tables in the correct order to handle the foreign keys.  
• Verify the table creation by running a SELECT statement for each table.  
• Import each CSV file into its corresponding SQL table.  
• Verify that each table has the correct data by running a SELECT statement for each.  

Attached in the repo, you will find each team member's VS file, ERD image, and SQL DB file with our individual solutions.   
The ETL_Mini_Project_SSims_KMcAtee_DLebron_FRuiz.ipynb is the aggregated file that includes the combined solutions the team presented Monday night.  


