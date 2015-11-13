## Implement a mobile app: Super Soccer Scores

#### App description

Create an account at http://www.football-data.org/. 
Use [the API](http://api.football-data.org/docs/latest/index.html) to build a simple mobile application (iOS or Android). 

See below the API endpoints you need to use:

1. `Endpoint 1. GET http://api.football-data.org/alpha/soccerseasons`: Returns a list of all seasons.
2. `Endpoint 2. GET http://api.football-data.org/alpha/soccerseasons/{season}/fixtures`: Returns fixtures for the given season.
3. `Endpoint 3. GET http://api.football-data.org/alpha/soccerseasons/{season}/leagueTable`: Returns league table for the given season.
 
Please, implement a 3-screen application:

- `Screen 1. Seasons list for 2015 year`: List all seasons. Use `Endpoint 1` to retrieve a list of soccer seasons. Limit it to the `Bundesliga 1` and `Bundesliga 2` and the current year only. On a season tap go to the `Screen 2` for that season.

- `Screen 2. League table for the specific season and last fixtures`: Use `Endpoint 2` to retrieve all results for the specific season and build a league table for it. You are not allowed to use `Endpoint 3` to receive league table and should provide logic to calculate it isntead. Please, see the implementation guide below and feel free to use `Endpoint 3` to compare with your result. You should cache locally calculated league table and update it when required. Please, put the results for the most recent match day above the results table as well. On team tap go to the `Screen 3`. Please, implement league table in the most flexible way, so changing scores calulation startegy won't be a problem in the future.

- `Screen 3. Results for the specific team`: This screen should contain all results for the specific team in the season selected on `Screen 2` in the form: `{DATE}: {TEAM A NAME} {GOALS TEAM A} - {GOALS TEAM B} {TEAM B NAME}`.

#### League table calculations simplified guide

- Every team receive 3 scores for win, 1 for draw and 0 for defeat. 
- If two teams has the same scores, the goals difference should be considered. The command with better goal difference should be on top.
- If two teams has the same scores and the same goal difference, the command which scored more goals should be on top.
- If the all above doesn't work use alphabetical order to define places.

#### Instructions

- Please, clone this repo in a new `Bitbucket` private repo.
- Implement `Super Soccer Scores` app there.
- Put in the repo short documentation on how to run the app, and if possible a link to the demo video.
- Grant access to your private repo for BitBucket user `supertag` so we can review your code.

Thanks in advance for your time spent on this test!
