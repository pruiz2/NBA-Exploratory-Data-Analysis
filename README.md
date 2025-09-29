# NBA-Exploratory-Data-Analysis
Exploring the data collected from the 2023-2024 NBA Season. I first converted the data from https://www.basketball-reference.com/leagues/NBA_2024_per_game.html, converted it from html to a csv file I could use for analysing data. I then skimmed through the datam checking column names, data values, as well as any empty values or 'DNP' (Did Not Play) values, that could skew the data processing. Drafting the schema for the database was next.

PKs: players(player_id), teams(team_id), games(game_id), boxscores(game_id, player_id).

FKs: boxscores.player_id → players, boxscores.team_id → teams, boxscores.game_id → games.

All of which were placed into a create_schema.sql file, and when ran in MySQL, will create the tables we can now use to ipload and then query the data.
