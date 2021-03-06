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

### In each page, I used the following sources for information (specific fixture and statistics). 
![fixture](https://user-images.githubusercontent.com/95297354/158028368-ba9e1d65-c8e1-41ba-b506-c6f472857a38.png)  ![statistics](https://user-images.githubusercontent.com/95297354/158028383-1b355bf7-7dc8-499a-9152-63f2782716cb.png)

### From the statistics table, I got the information about the teams and the game stats
![team_names](https://user-images.githubusercontent.com/95297354/158028789-ea4ef2bb-b748-47d1-ae30-a59475fdc004.png) ![statistics_part](https://user-images.githubusercontent.com/95297354/158028796-63972fc6-5f58-4439-b67f-07c1100d3685.png)

### Considering the game stats, each trow was related to a specific category (goals, assists, etc.)
![each_trow_is_category](https://user-images.githubusercontent.com/95297354/158028869-4f5dbdee-d1f2-4d95-a439-ca20468f617b.png)

### Inside each "trow" there was info about the category, home_team statistic and away_team statistic
![inside_trow](https://user-images.githubusercontent.com/95297354/158028919-3dca99d2-36fc-400f-961c-11f721126145.png)

### Then I noticed that for each statistic, the "pattern" of the html code was the same 
### For goals
![equal_class_1](https://user-images.githubusercontent.com/95297354/158028961-edd2ebe9-5cba-4dc5-968e-38e0913ef975.png) 
### For headers
![equal_class_2(headers)](https://user-images.githubusercontent.com/95297354/158028973-2d1143fa-6d7e-4b01-9e5f-cbc71b0db0af.png)

### The final step before scraping the information, was to create an empty dataframe with the appropriate columns
![empty_df](https://user-images.githubusercontent.com/95297354/158029081-7f717af1-17a9-4499-ad1a-d3c5fd6fdba2.png)

### The code 
![coding](https://user-images.githubusercontent.com/95297354/158029108-ecbb2a0f-499f-4a16-ac56-8f9af2d5caff.png)

### The obtained dataframe 
![DATAFRAME](https://user-images.githubusercontent.com/95297354/158029214-be048d01-43dd-4dd1-b3d7-e0a99efe1295.png)



