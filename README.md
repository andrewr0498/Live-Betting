# Live Betting Project

The purpose of this project is to develop a model that allows us to identify favorable live bets during NBA games. Sportsbooks will offer live lines during games that in theory reflect the win probabilities in game but in practice swing pretty wildly and a model could in theory take advantage of this to identify favorable plays and hedges. For our purposes the primary initial challenge of this is going to be collecting data on sportsbooks and the lines they offer during games, which is going to be a potentially complex data scraping operation. We concurrently want a model we think will give us trustworthy win probabilities to compare the live lines against. This is a potentially multiple semester project and we should start with our focus on getting the data because that kind of dataset in itself is potentially valuable and doesn’t really publicly exist.

If you are unfamiliar with some of the concepts above here are a few resources for you to look over to get started:

* [What is a money line?](https://www.thelines.com/betting/moneyline/)
* [Bovada NBA Live Betting Odds](https://www.bovada.lv/sports/basketball/nba)
* More to come

Collecting the data for this project is going to be an incredibly complex part of what we need to do this semester. Continuously scraping data from a site like Bovada above is almost definitely going to require using an API. Unfortunately no sports betting sites that I know of offer an API, (let me know if you find one) but [this](https://jsonodds.com/home/) is the best that I found (but it costs money). Regardless, here are a couple tools that I anticipate we are going to need and you should familiarize yourself with if you do not know them already:

* [HTML Elements](https://www.w3schools.com/html/html_elements.asp)
* [BeautifulSoup](https://pypi.org/project/beautifulsoup4/)
* [APIs](https://en.wikipedia.org/wiki/Application_programming_interface), specifically the one above
* More to come

It is very important for all of us to meet on a weekly basis (preferably at the same time every week) to make sure that we are all on the same page and know what our tasks for the week are, please fill out [this](https://www.when2meet.com/?7553455-poVDL) form ASAP so that we can determine our weekly meeting time.