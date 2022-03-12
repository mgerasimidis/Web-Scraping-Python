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

### In each of these links, in order to get inside each game, we should get access in the circled arrows. Moreover, we should take care of the days that the games happened.
![get_inside_games](https://user-images.githubusercontent.com/95297354/158027989-3e473545-d4af-4fc3-89c2-1f825937fed1.png)

### In each game there were different tables, but I wanted the statistics table as shown in the picture below. What needed was to add in the end of each game link the following string "/statistics".
![statistics_1](https://user-images.githubusercontent.com/95297354/158028286-8ce885b4-e14d-4275-b194-008f53760f20.png)

### In each page, I used the following sources for information (specific fixture, stadium and statistics). 
![fixture](https://user-images.githubusercontent.com/95297354/158028368-ba9e1d65-c8e1-41ba-b506-c6f472857a38.png)  ![statistics](https://user-images.githubusercontent.com/95297354/158028383-1b355bf7-7dc8-499a-9152-63f2782716cb.png)


