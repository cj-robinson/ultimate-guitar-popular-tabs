Overview
---
This repository holds the files for the final project for Data & Databases in Columbia's M.S. in Data Journalism. Using Selenium and requests, I scrape the [most popular songs](https://www.ultimate-guitar.com/explore?order=hitstotal_desc) on [www.ultimate-guitar.com](www.ultimate-guitar.com/), a website dedicated to learning how to play songs on the guitar through community-contributed tabs and chords. I also include artist country of origin to output into an interactive map.

Goals
---
Data & Databases was an in-depth explanation of how to think about dataset creation and storage. We learned to query from relational databases in SQL, pull from APIs and scrape webpages. In the final project, I wanted to do a multi-page scrape that would systematically find links for the top songs that guitar players regularly learn and join it with additonal metadata about the kinds of artists represented in that dataset.

Process
---
I first scraped the data from the top 5,000 songs on the [all-time popularity leaderboard](https://www.ultimate-guitar.com/explore?order=hitstotal_desc). It included links to the song pages as well as title, artist, views and star rating averages. I used BeautifulSoup and Selenium to pull these into a dataset. Using those links, I then scraped individual songs for additional metadata like the key of the song or capo placement, as well as the full text and chords, appending this data to the original dataset. Finally, using an open-source API, I added available information about the artist of each song. 

Learnings
---
This project was an exercise in patience! Because I had to use Selenium to load the page, wait for any JavaScript elements to load and then scroll down the page, each song took 3-4 seconds. I split the 5,000 into multiple sections to function as checkpoints, but I wish I did this more often and did it in a more programatic way utlizing more loops to account for timeouts or other interruptions. 

Files
---
*1_ug_top_songs.ipynb* - Initial scrape of top 5,000 tabs and links based on views on ultimate-guitar.com

*2_ug_ind_songs.ipynb* - After initial scrape of the top 5,000 tabs on ultimate-guitar.com, scrape each individual tab for metadata/chords

*3_mb_artist_data.ipynb* - Take artist names and search for them on the Music Brainz API, an open source encyclopedia for artist information

*4_collate.ipynb* - Take all tabs missed from individual scrape and rescrape, then collate all CSVs together

*5_map_graphs.ipynb* - Take full data and add country geometry, then does some exploratory analysis

*top_songs_full.csv* - Final collated dataset

*map_templates/* - files for map of country counts of top tabs

*data/* - raw csvs from initial scrapes



