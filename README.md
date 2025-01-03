This repository holds the files for the final project for Data & Databases in Columbia's M.S. in Data Journalism. Using Selenium and requests, I scrape the [most popular songs] (https://www.ultimate-guitar.com/explore?order=hitstotal_desc) on [www.ultimate-guitar.com](www.ultimate-guitar.com/), a website dedicated to learning how to play songs on the guitar through community-contributed tabs and chords. I also include artist country of origin to output into an interactive map.

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



