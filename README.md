# Money Tiger Scraper

A helper utility based on [money-tiger-scraper-docker](https://github.com/BackSlasher/money-tiger-scraper-docker).
Use this if you don't want to run the scraper locally on your infra, and utilize github instead

## Instructions
1. Prepare the following:
   1. API token from the Money Tiger website.
   2. Config JSON, containing all of the companies you want to scrape and your account credentials
1. Fork this repository. The fork can be private.
2. Go to your fork's repository settings, edit secrets (actions), and add the following secrets:
   1. `API_TOKEN`: Your token
   2. `CONFIG`: The config JSON.
1. If you wish, edit the actions yaml (`.github/workflows/scrape.yml`) and modify the cron expression to scrape at different time.

You're all set! You can manually trigger an action, or wait for the cron time to arrive.
Success/failure can be viewed in "actions", detailed results can be viewed in the Money Tiger UI.

## Updates
The GitHub action is update the Docker image for the scraper before running it, don't worry about keeping your fork up to date.
As long as you're getting your data, your'e good
