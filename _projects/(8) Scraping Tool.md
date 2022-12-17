---
name: Scraping Tool
tools: [Python, Api, Gui, Twitter, Cron, Tweets, Tkinter, Tweepy, Scraping-Python]
image: ../assets/img/portfolio/scraping_tool/scraping_tool.png
description: A Python application providing a GUI to specific functions from Tweepy library and scripts allowing CRON jobs.
---

{% include elements/figure.html image="https://github.com/Wazzabeee/scraping_tool/blob/main/src/images/screenshots/search_tab.PNG?raw=true" caption="Search Tab" %}
## About
This program allow the user to retrieve tweets from Twitter's API using the library Tweepy via a GUI or a CRON automatization.

This project was made part of my internship at the "Human Computer Humans Interacting with Computers at University of Primorska" lab (HICUP Lab).

## Setup
To use this program, you will need your API keys retrieved after [creating a developer account at Twitter](https://developer.twitter.com/en/apply-for-access).

Once retrieved the keys must be filled as follows.
{% include elements/figure.html image="https://github.com/Wazzabeee/scraping_tool/blob/main/src/images/credentials.png?raw=true" caption="credentials.py" %}

## How to use
```bash
# Clone this repository
$ git clone https://github.com/scraping_tool

# Go into the repository
$ cd scraping_tool

# Install requirements
$ pip3 install -r requirements.txt

# Fill credentials in credentials.py
# See "Setup"

# Run the app
$ python main.py
```

## Parameter details
More details on the parameters available can be seen on [Twitter's offical page](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/search/api-reference/get-search-tweets).

## CRON automatization
After trying out queries and requests with the GUI, you can setup automatizations.

You can define the parameters of the search via the `cron_search.json` file (or `cron_user.json`). All parameters are the same from the GUI’s tab.

When you’re ready you just have to setup the execution of the `cron_search.py` (or `cron_user.py`) script at the desired times and days.

## Used Software and Libraries
- Programming language: Python
- Libraries: Tweepy, Pillow, Tkinter
- Source control: GitHub
- Other tools: PyCharm

<p class="text-center">
{% include elements/button.html link="https://github.com/Wazzabeee/scraping_tool" text="Code" %}
</p>
