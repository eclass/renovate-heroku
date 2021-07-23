# renovate-heroku

A heroku button to deploy renovate-heroku.

## Deploying to Heroku

```bash
heroku create
git push heroku master
```

Alternatively, you can deploy your own copy of the app using the web-based flow:

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/eclass/renovate-heroku)


## Add cron job

Open Scheduler Dashboard with:
```bash
heroku addons:open scheduler
```

On the Scheduler Dashboard, click “Add Job…”, enter a task, select a frequency, dyno size, and next run time.

Add `renovate $RENOVATE_REPOS`, select Daily and "00:00" to run renovate every day at midnight.
