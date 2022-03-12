# Web Scraping with Python
Getting data from the original website of [greek super league](https://www.slgr.gr/el/) about each game from seasons 2006-2007 to 2021-2022. My purpose is to do an exploratory data analysis on these data at a later point.

## Prerequisites
* Requests
* BeautifulSoup
* pandas 

## Walk-through of the project

Considering the [schedule page](https://www.slgr.gr/el/schedule/), there are two things to consider at first:

### Seasons:
![seasons_1](https://user-images.githubusercontent.com/95297354/158027668-b06b760c-91b0-417a-af3b-e8ce699ddfb2.png) until ...  ![seasons_2](https://user-images.githubusercontent.com/95297354/158027727-900d3dc2-9028-424a-bba3-14f8c6c282f6.png)


### Super league games (and not play off's / play out's):
![league](https://user-images.githubusercontent.com/95297354/158027596-1d8a2796-f758-4180-9afa-1c11d75302b9.png)


### Here we get a list of links, about each season and only the Super league games:
![sl_seasons](https://user-images.githubusercontent.com/95297354/158027789-0109f633-4c33-4508-8d16-dd18019799b0.png)

### In each of these links, in order to get inside each game, we should get access in the circled arrows:
![get_inside_every_game](https://user-images.githubusercontent.com/95297354/158027840-1b2a100c-62d9-4737-a0f8-a2321a087c60.png)
