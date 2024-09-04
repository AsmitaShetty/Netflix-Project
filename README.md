# Netflix-Dashboard

### Dashboard Link : [Netflix Dashboard](https://app.powerbi.com/groups/me/reports/fe0d47cf-3e0e-4d8e-a8a2-e18824138816/ReportSection).

## Problem Statement

This project involves analyzing a dataset containing a comprehensive list and metadata of all TV shows and movies available on Netflix, which was sourced from the IMDb website. The dataset includes around 7,000 records and contains various attributes related to the content, such as titles, ratings, genres, and more. The primary goal of this analysis is to gain insights into the Netflix library using Power BI by preparing the data, building a data model, and creating interactive visualizations.


### Dataset Information

The dataset is provided in a CSV file named netflix_list.csv and contains the following columns:

imdb_id: Unique show identifier.
title: Title of the show.
popular_rank: IMDb popularity rank.
certificate: Age certification of the show (contains null values).
startYear: Year when the show first aired.
endYear: Year when the show ended (if applicable).
episodes: Number of episodes (1 for movies).
type: Indicates whether the entry is a movie or series.
orign_country: Country of origin.
language: Language of the show.
plot: Synopsis of the show.
summary: Summary of the show's storyline.
rating: Average rating of the show on IMDb.
numVotes: Number of votes the show received.
genres: Genre(s) the show belongs to.
isAdult: Indicates if the content is for adults (1 for yes, 0 for no).
cast: List of main cast members.
image_url: URL link to the show's poster image.

# Steps Followed

1. Data Preparation and Transformation

Data Ingestion:

Loaded the netflix_list.csv file into Power BI.
Promoted the first row as headers to label each column appropriately.
Data Type Conversion:

Converted columns to appropriate data types, including text, integers, and floating-point numbers, as needed.
Column Removal:

Removed irrelevant columns: popular_rank, certificate, endYear, episodes, language, summary, isAdult, and cast.
Column Renaming:

Renamed columns for better readability and consistency:
imdb_id to ID
title to Title
startYear to Start Year
runtime to Run Time
type to Type
orign_country to Country
plot to Plot
rating to Rating
numVotes to Votes
genres to Genres
image_url to Image URL
Data Cleaning:

Replaced null or "\N" values with appropriate placeholders.
Converted the Run Time column to an integer data type.
Row Filtering:

Filtered out rows where the Rating is null or where the Country is "-", or where the Type is categorized as "short," "video," or "videoGame".

2. Data Model

Background and Visualization
Created a gradient with color codes ranging from #000000 to #FFFFFF.
Developed a custom background using PowerPoint to enhance the visual appeal of the dashboard.

3. DAX Measures & Calculated Columns
- #Titles: Count of unique titles (DISTINCTCOUNT of netflix_list[ID]).
- #Votes: Total number of votes (SUM of netflix_list[Votes]).
- Votes per Title: Average number of votes per title (DIVIDE([# Votes], [# Titles])).
- Average Rating: Average rating of all titles (AVERAGE of netflix_list[Rating]).
- Genre: Extracted the primary genre from the Genres column.
- Listing Type: Categorized content as either "Movie" or "Television" based on the Type column.
- Rating Group: Created rating groups based on a range of rating values.
- Dynamic Rating Fill: Applied conditional formatting to fill visuals based on rating groups.
- Dynamic Rating Font: Applied conditional font colors based on rating groups.
- Listing Type Filter: Applied filters to differentiate between Movies and TV Shows.

![image](https://github.com/user-attachments/assets/38c65376-bc81-4055-a453-4174752cc91e)

4. Visualizations Created

Funnel Chart: Visualized the distribution of content across categories.

![image](https://github.com/user-attachments/assets/61a30798-d3de-4555-991c-1502b8d78aef)

New Card with Reference Labels: Enhanced data display with dynamic labels.

![image](https://github.com/user-attachments/assets/a9fbf59f-aa7d-4906-8396-bfb5ba9713d7)

Table with Images: Displayed shows alongside their image URL.

![image](https://github.com/user-attachments/assets/6ea3fe72-7c60-45ac-ba61-cf696cbc5dcf)

New Slicer Filter: Allowed dynamic filtering of data based on selected criteria.

1.
![image](https://github.com/user-attachments/assets/5c5db67a-dba3-4d81-bdba-f49ff143046b)

2.
![image](https://github.com/user-attachments/assets/8ff1360b-7f8f-4bcb-a1f5-3c5bc07688c1)

Bar Chart with Secondary Stepped Line Axis: Created a combined bar and line chart for comparative analysis.

![image](https://github.com/user-attachments/assets/87115d60-6c0f-4cfa-ad1a-1703b6151234)

Table with Databars and Conditional Formatting: Visualized metrics with databars and applied conditional formatting for better readability.

![image](https://github.com/user-attachments/assets/bce05aa2-7af5-4a19-8044-8c177ab4226d)

Azure Map with Size Parameter Filters: Mapped content based on origin countries with size parameters reflecting different metrics.

![image](https://github.com/user-attachments/assets/cedfdd5a-e71f-4dec-9f6e-e36c50f3fd19)

# Snapshot of Dashboard

![image](https://github.com/user-attachments/assets/8ab5b4fc-cdc3-4981-9f83-a93e4168e295)

# Conclusion

This project showcases a thorough analysis of Netflix's content library, leveraging Power BI's capabilities to deliver insights into the data through well-crafted visuals and measures.
