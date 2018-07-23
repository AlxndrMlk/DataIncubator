# Dataset description

## Sources of data
The dataset has been generated using two sources:
* Archive of Billboard Hot 100 (e.g. https://www.billboard.com/archive/charts/2018/hot-100)
* Spotify API

## Obtaining data - method
Billboard Hot 100 archive was scraped using Python script. The obtained data (song titles and artists' names for a given year) 
was parsed using Beautiful Soup Python library.
Then additional editing script was applied to the data to prepare search phrases for Spotify API.
Next Spotify API was requested to find a song based on search phrase and return song's Spotify ID.
Spotify ID was used to get detailed track information (tempo, key, mode, etc.) from Spotify API.

## Data structure
All obtained information of interest had been put into a pandas DataFrame and saved for further analysis.

