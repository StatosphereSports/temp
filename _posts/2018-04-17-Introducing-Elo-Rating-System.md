---
layout: post
title: "Introducing the Statosphere Elo AFL Rating System"
date: 2018-04-17
---

The Statosphere Elo AFL Rating System (SEARS) builds on the concept put together by the late Hungarian Physicist Arpad Elo, designed as a Chess rating system.

The Elo rating system is now probably most famous in popular society as the main rating system used by Five Thirty Eight for their sports prediction models. It has also been used quite commonly in AFL circles by a number of people including Matter Of Stats, Plus Six One and The Arc, all of whom have provided inspiration in their own way for the shapre of the current model that I am running.

The current Elo rating system consists of an Offensive and Defensive rating for each team, these ratings are both centered around 0 with a positive rating indicating they are better than average at the given metric and a negative rating indicating worse than average. Each side also has an offensive and defensive rating at every AFL ground that they have played at more than 30 games at over their history.

Each match the two competing teams 4 ratings (Offensive, Defensive, Venue Offensive and Venue Defensive) as well as the average score from previous season are used to predict the score for each side and the margin, as well as a probability of victory.

Below is an example of the calculations behind the prediciton of the most recent match played, at the time of writing, between Geelong and St Kilda.

Geelong Predicted Score

Geelong Offensive Rating: 4.6169

Geelong Offensive Rating (Kardinia Park): 3.3921

St Kilda Defensive Rating: -1.5739

St Kilda Defensive Rating (Kardinia Park): -8.4091

Geelong Predicted Score  = Average Score (2017) + Geelong Offensive Rating - St Kilda Defensive Rating + Geelong Offensive Rating (Kardinia Park) - St Kilda Defensive Rating (Kardinia Park)

Geelong Predicted Score = 89.0990 + 4.6169 - (-1.5739) + 3.3921 - (-8.4091) = 107.0911


St Kilda Predicted Score

St Kilda Offensive Rating: -7.4197

St Kilda Offensive Rating (Kardinia Park): -3.3872

Geelong Defensive Rating: 2.1315

Geelong Defensive Rating (Kardinia Park): 5.7304

St Kilda Predicted Score  = Average Score (2017) + St Kilda Offensive Rating - Geelong Defensive Rating + St Kilda Offensive Rating (Kardinia Park) - St Geelong Defensive Rating (Kardinia Park)

St Kilda Predicted Score = 89.0990 + (-7.4197) - 2.1315 + (-3.3872) - 5.7304 = 70.4302


Therefore the model predicted a 39 point Geelong win, 107-70. In reality the final margin was a 49 point Geelong win, 103-58. This new information is then input into the model to improve its predictions going forward.

At the end of each season due to the competitive balance measures in place such as the draft, salary cap and depending on who you speak to free agency, it is reasonable to assume that sides should regress towards the mean. For this reason, and through interative testing, I have included a 70% regression of teams Offensive and Defensive ratings over each offseason. For this reason, predicted results tend to be closer at earlier stages of the season when the good teams aren't considered as good as they are and the bad teams aren't considered as bad as they are.

