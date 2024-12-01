# Team 8 Mist 4610 Group Project 1

## Team Name: 
select * from MIST4610 where grade = A; 

## Team Members:

1. Gus Wilkerson [@augwilk](https://www.github.com/augwilk)
2. Emma Calleja [@EmmaCalleja](https://github.com/EmmaCalleja)
3. Hannah Conley [@Hmc98563](https://github.com/Hmc98563)
4. Rahil Patel [@rahilp0215](https://github.com/rahilp0215)
5. Marc Ordonio [@marcord245](https://github.com/marcord245) 


## Problem Description:

The task at hand:
Today, college football data is spread across multiple platforms and sources, making it difficult to get a clear and accurate picture of the sport. Since this approach is broken up across platforms, it is difficult to access and analyze key statistics or trends over time. To address this issue, the NCAA has launched a project to create an essential database of Division 1 college football statistics.
Specifically, the project aims to create a unified data repository for all D1 conferences, players, and head coaches, including in-depth statistics such as NIL, wins, losses, and game statistics among others.


## Data Model

Explanation of data model: 

Our data model is based around the landscape of college football as we see it. College football is made up of a handful of conferences each of which has several teams as shown by the one to many relationship established between the conference and team entities. The team entity contains pertinent information for a specific team including what university of the team and the tally of their wins and losses.

Teams need several coaches to operate (i.e. position coaches, coordinators, trainers) but each has just one head coach as shown by the one to one relationship between the coach and team entities. Coaches have a name, a salary, and a title of their position.

Each team plays in multiple games in a year and each game has two teams. The weak entity linking the many to many relationship between team and game is the team_game entity which stores each team’s individual score in the specific game. 

Because of the transfer portal, players can now be on multiple teams over the time of their collegiate career but only one team at a time. The portal entity links many players to many teams and vice versa, storing the date they joined and left the team if applicable. 

The player table stores personal information for each player such as their name, birthdate, number, and position. A player plays in many games and a game has many players involved. The weak entity between these two entities is gameStats which stores the offensive yardage statistics each player records in each game they play. Passing yards, receiving yards, and rushing yards for each player are stored here.

A player can also now have many NIL deals with several companies. One company (stored in the Sponsor table) also has the ability to sponsor many players. A sponsor has a company name and a unique id. To link the many to many relationship between Sponsor and player there is the NIL table. The NIL table stores the id of the deal as well as the agreed upon dollar amount for the contract between a company and a player.

Our data model stores a range of data regarding college football which could be useful for a school administration, third party company interested in sponsoring athletes, or the everyday college football fan!




## Data Dictionary:



## Query Type Matrix:

![Screen Shot 2024-10-13 at 8 29 41 PM](https://github.com/user-attachments/assets/cf262f29-f47f-43a4-8608-b380128479d1)



## Queries:



## Visualzations:





## Database information:

Name of the database: cs_aww39979

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: 
CALL TP_Q1();
