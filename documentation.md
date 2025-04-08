-----------As a first step to extract meta data and load it into csv and plot simple barchart-----------
Import Necessary Libraries:

>Import libraries required for API interaction, data manipulation, and visualization.
>Set Up API Authentication:
>Obtain client credentials (Client ID and Client Secret) from the Spotify Developer Dashboard.
>Configure the Spotify API client using these credentials for authentication.

Define the Track URL:
Specify the full URL of the desired Spotify track from which you want to extract data.

Extract Track ID:
Use regular expressions to parse the track URL and extract the unique track ID.

Fetch Track Details:
Use the Spotify API to retrieve detailed information about the track using the extracted track ID.

Display Track Metadata:
Print or log the fetched track details to review the metadata, including attributes like track name, artist, album, etc.

Transform Data:
If necessary, clean and structure the fetched data for analysis or storage. This may involve organizing it into a specific format or extracting relevant fields.

Load Data into Storage:
Save the transformed data into a CSV file for easy access and sharing.

--------------------Extract multiple track data from spotify api---------------------
>Read Track URLs from File
File Input: Reads a list of Spotify track URLs from a text file (track_urls.txt). Each line in the file represents a unique track URL.

>Process Each Track URL
Loop Through URLs: Iterates over each URL in the list.

>Prepare Data for Database Insertion
Data Mapping: Organizes the fetched metadata into a dictionary (track_data) with keys like Track Name, Artist, and Duration (minutes).

>Insert Data into MySQL Database
SQL Query: Uses an INSERT statement to add the track metadata to the spotify_tracks table.

Parameter Binding: Safely injects the track data into the query using placeholders (%s) to prevent SQL injection.

Commit Changes: Saves the transaction to the database after each insertion.
