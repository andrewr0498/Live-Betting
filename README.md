# Live Betting Project

### Overview and Purpose

The purpose of this project is to develop a model that allows us to identify favorable live bets during NBA games. Sportsbooks will offer live lines during games that in theory reflect the win probabilities in game but in practice swing pretty wildly and a model could in theory take advantage of this to identify favorable plays and hedges. For our purposes the primary initial challenge of this is going to be collecting data on sportsbooks and the lines they offer during games, which is going to be a potentially complex data scraping operation. We concurrently want a model we think will give us trustworthy win probabilities to compare the live lines against. This is a potentially multiple semester project and we should start with our focus on getting the data because that kind of dataset in itself is potentially valuable and doesn’t really publicly exist.

### Background Information

If you are unfamiliar with some of the concepts above here are a few resources for you to look over to get started:

* [What is a money line?](https://www.thelines.com/betting/moneyline/)
* [Bovada NBA Live Betting Odds](https://www.bovada.lv/sports/basketball/nba)
* More to come

### Technical Resources

Collecting the data for this project is going to be an incredibly complex part of what we need to do this semester. Continuously scraping data from a site like Bovada above is almost definitely going to require using an API. Unfortunately no sports betting sites that I know of offer an API, (let me know if you find one) but [this](https://jsonodds.com/home/) is the best that I found (but it costs money). Regardless, here are a couple tools that I anticipate we are going to need and you should familiarize yourself with if you do not know them already:

* [HTML Elements](https://www.w3schools.com/html/html_elements.asp)
* [BeautifulSoup](https://pypi.org/project/beautifulsoup4/)
  * to start it wouldn't be too hard to just use BeautifulSoup to scrape Bovada like every second for an NBA  game that is going on
  * The problem with this is we would literally just have to have a py file or jupyter cell that runs continuously over the course of a NBA game which is just kind of a pain in the ass
  * I guess this would be a good way to start making an initial dataset since we can write it to a csv
  * But we wouldn't have any historical data, we would only have data for the times this spring that we decide to run the code
  * And idk how fast the BeautifulSoup requests will be. It's possible they'd be too slow and would miss some changes to the moneylines
* [APIs](https://en.wikipedia.org/wiki/Application_programming_interface)
  * [JsonOdds](https://jsonodds.com/home/) (the one above)
  * [Fantasy Data](https://fantasydata.com/sports-data/nba-api)
  * [Don Best](https://pypi.org/project/donbest/) this one looks promising
  * shit. it looks like all of these cost money
  * Calvin found [this one](https://github.com/pinnacleapi/pinnacleapi-documentation), looks pretty good
  * Haoran found [this one](https://therundown.io/odds/nba)
    * if you click on a game they even have graphs of how the moneyline changes during the course of the game
 * [Web scraper](https://github.com/ntran16/CalFootball_4thDown/blob/nate_branch/n_most_similar_games.ipynb) I made from last semester for reference
* More to come

### The data we want

Ideally we can get data in a format like the table I made up below. For any given NBA game, an entry should be added to our dataset whenever the moneyline changes in game.

This is slightly optimistic since I don't expect a change in the moneyline to occur at the exact same time as a play occurs, but if we have the UTC timing of each then I think we could look into the impact of certain plays in certain situtations on the moneyline. I haven't followed moneylines close enough, but I think that they sometimes change without any play happening, so there could be entries in our dataset without a play description.

|Date/Time|HomeTeam|AwayTeam|Favorite|Underdog|HomeTeamFavorite|HomeScore|AwayScore|GameClock|Quarter|PlayDescription|
|---|---|---|---|---|---|---|---|---|---|---|
|2018-11-22 19:53:42|Warriors|Lakers|-303|+157|True|78|66|7:55|3|Steph Curry makes...|
|2018-11-22 19:53:55|Warriors|Lakers|-320|+166|True|78|66|7:50|3|Lebron James turnover...|
|2018-11-22 19:54:22|Warriors|Lakers|-315|+161|True|78|66|7:32|3|Draymond Green misses...|

### Meetings

It is very important for all of us to meet on a weekly basis (preferably at the same time every week) to make sure that we are all on the same page and know what our tasks for the week are, please fill out [this](https://www.when2meet.com/?7553455-poVDL) form ASAP so that we can determine our weekly meeting time.

### Questions for Daniel

1. First off, is the example dataset above kind of like what you had in mind? Is there something else you'd want to add?

2. Were you thinking of only using moneyline? Or did you want spread too? Could you explain what you wanted to do with win probability?
