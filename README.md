<h1>Project Title</h1> 
Video Game Sales Analysis

<h2>Short Description</h2>
This repository contains Python scripts for analyzing video game sales data using pandas, SQLalchemy, and MySQL. The code performs various data analysis tasks such as filtering games based on launch years, querying sales statistics from a MySQL database, and generating insights about publishers and genres.
#Getting Started

<h2>Getting Started</h2>
<h3>Prerequisites</h3>
To run the code in this repository, you'll need:
- Python (version 3.6 or higher)
- pandas library (pip install pandas)
- SQLAlchemy library (pip install sqlalchemy)
- pymysql library (pip install pymysql)
- You also need access to a MySQL database with a table named vgsales containing video game sales data.

Python and the listed libraries are necessary for data processing, pandas for DataFrame manipulation, SQLAlchemy for database connectivity, pymysql for MySQL interaction.

<h4>Installing</h4>
- pip install pandas 
- pip install sqlalchemy 
- pip install pymysql

<h2>Running the Tests</h2>
<h3>Breakdown of Tests</h3>
Part 1 - Analyzing Games from 2000-2005:

This test involves executing the part1 script, which utilizes the pandas library to read the video game sales data from a CSV file or a database into a DataFrame. The script then filters the DataFrame to include only the games launched between 2000 and 2005 based on the "Year" column. 

- Import the pandas library and assign an alias 'pd' .
- Variable 'input_file_path' is created to store the file path of the CSV file containing video game sales data. The 'r' before the string denotes a raw string literal, which is used to prevent issues with backslashes in file paths.
- 'read_csv' function to read the CSV file specified by 'input_file_path' and load its contents into a DataFrame called 'input_raw_data'.
- The '.head()' method is used to display the first few rows (by default, the first five rows) of the DataFrame 'input_raw_data'.
- Similarly, the '.tail()' method is used to display the last few rows (by default, the last five rows) of the DataFrame 'input_raw_data'.
- DataFrame 'input_raw_data' to include only the rows where the "Year" column falls within the range from 2000 to 2005. The filtered DataFrame is stored in a new variable called 'between_00_05'.
- 'print()' function is used to display the contents of the DataFrame 'between_00_05', which now contains only the games launched between 2000 and 2005.


Part 2 - Database Connection and Data Retrieval:

Before running this test, ensure that the necessary Python libraries (pandas, SQLAlchemy, pymysql) are installed. The part2 script establishes a connection to a MySQL database using SQLAlchemy's 'create_engine' function. Provide the appropriate database connection URL with credentials and the database name. Once connected, the script executes an SQL query to fetch data from the vgsales table and stores the results in a pandas DataFrame. This test verifies the successful retrieval of data from the database and its representation in a structured format for analysis.

- Here, an engine object is created using SQLAlchemy's 'create_engine' function, specifying the MySQL ('mysql+pymysql') and the connection details (username, password, host, database name). The engine object is then used to establish a connection ('conn') to the MySQL database.
- This line executes an SQL query "SELECT * FROM Data1202.vgsales" on the connected MySQL database ('conn') and stores the result in a pandas DataFrame called 'df'. The query selects all columns (*) from the vgsales table in the Data1202 schema.
  
Part 3 - Advanced Data Analysis:

Execute the part3 script, which combines both SQL queries and pandas operations for advanced data analysis. The script executes a complex SQL query on the MySQL database, filtering data based on specific criteria such as genre and launch year. It performs aggregation functions (e.g., sum, round) to calculate sales statistics such as total sales in different regions (NA, EU, JP) and global sales. The script also calculates the percentage share of North American sales in the global market for a particular genre. These calculations are then presented in a pandas DataFrame.

- Filtering data in Python using a condition "(df['Publisher'] == 'Nintendo')" to select rows where the Publisher is 'Nintendo'. The filtered DataFrame is assigned to 'nintendo_games', and its first few rows are displayed. The 'len()' function is used to calculate the number of Nintendo games and print the result.
- The code filters the DataFrame df to include only rows where the Genre is 'Action' and the Year is greater than or equal to 2005. The '.head()' method displays the first few rows of the filtered DataFrame, and the '.max()' method is used to find the maximum value of 'EU_Sales' in the filtered data.
- Include only rows where the Year falls between 2000 and 2005. It then prints the filtered DataFrame 'between_00_05', which contains data for games launched between 2000 and 2005.
  
<h2>Deployment</h2>
This project can be deployed locally on your machine for data analysis and insights generation.

<h2>Author</h2>
Omar Al-Trad

<h2>License</h2>
None

<h2>Acknowledgment</h2>
I would like to extend thanks to Mr. Omar Al-Trad for the dedicated efforts and valuable contributions throughout the development of this project. His expertise and commitment have been instrumental in achieving project goals and ensuring its success.
