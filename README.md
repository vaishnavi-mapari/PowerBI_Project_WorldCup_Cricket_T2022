# Power BI Project: T20 World Cup 2022 Cricket Analysis

![Project Overview](https://user-images.githubusercontent.com/123319398/227054573-45233466-c321-4a49-9071-fa3a86d62a23.png)

## About This Project
This Power BI project analyzes the performance of players in the T20 World Cup 2022, showcasing the top players from different teams and identifying the best 11 players of the tournament.

### Data Source
The data was sourced through web scraping the ESPN website using BrightData. The extracted data was in JSON format. We used Jupyter Notebook to convert the JSON files into dataframes and subsequently into CSV files for further analysis in Power BI.

### Data Cleaning and Transformation
Data cleaning and transformations were performed using Power Query Editor in Power BI. Here are the key steps:

#### **In `dim_players`:**
- **Renaming Files:** Standardized column names for consistency.
- **Header Adjustment:** Set the first row as the header.
- **Splitting Name Column:** Separated player names into first and last names.
- **Removing Duplicates:** Ensured data integrity by eliminating duplicate records.

#### **In `dim_match_summary`:**
- **Custom Column Addition:** Added a 'stage' column to categorize games into 'Qualifier' or 'Super 12'.
- **Datatype Change:** Converted the 'stage' column to text for consistency.

#### **In `fact_bowling`:**
- **Column Renaming:** Renamed 'Bowling Team' to 'Team' for uniformity.
- **Ball Calculation:** Created a 'Ball' column from the 'Overs' column by splitting it (e.g., 2.5 overs into 2 overs and 5 balls).
- **Null Value Handling:** Replaced null values with 0.

#### **In `batting_summary`:**
- **Column Renaming:** Standardized column names (e.g., '4s' to 'Fours', '6s' to 'Sixes', and 'Team Innings' to 'Team').
- **Out/Not Out Conversion:** Converted the 'Out/Not Out' column to a binary format, with 'Out' = 1 and 'Not Out' = 0.
- **Datatype Adjustment:** Changed the datatype of the 'Balls' column to a whole number.
- **Text Removal:** Removed text after the player's name in the 'Batsman_Name' column.

### Power BI: Data Import, Modeling, and Visualization
After data cleaning, CSV files were imported into Power BI. The following steps were taken to create an insightful dashboard:

- **Data Modeling:** Established relationships between tables for accurate data analysis.
- **Power Query Editor:** Applied additional transformations as needed.
- **DAX Measures:** Created custom calculations to derive meaningful insights.
- **Dashboard Design:** Designed an interactive dashboard using features such as bookmarks, tooltips, matrices, scatter charts, area charts, buttons, slicers, and more.

![Top Opening Batsmen](https://user-images.githubusercontent.com/123319398/222763389-5d931ad6-f84a-4eaf-9c4e-ed1ae2aa09b1.png)
*This visual shows the top opening batsmen, their batting averages, strike rates, boundaries scored, and the number of balls faced.*

![Best 11 Players](https://user-images.githubusercontent.com/123319398/222764003-131dda43-f2fb-42ca-adf2-f77a3ef6a22f.png)
*This visual showcases the best 11 players of the T20 World Cup and their performance.*

### Player Analysis Using Tooltips
Tooltips were used to provide detailed player analysis when hovering over specific data points.

![Player Analysis Tooltip](https://user-images.githubusercontent.com/123319398/222764485-dc14f453-67e0-4913-b2c7-345912cb7aae.png)
