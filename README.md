# Team 8 Mist 4610 Group Project 2

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

Our data model is based around the landscape of college football as we see it. College football is made up of a handful of conferences each of which has several programs as shown by the one to many relationship established between the conference and program entities. Each season a program has a different team. The team entity contains pertinent information for a specific team for a given season including what university of the team and the tally of their wins and losses. Every season, a conference has 1 team crowned as the conference champion.

Every program has another program taht is its arch rival indicated by the recursive 1 to 1 relationship within the program entity. Programs also need several coaches to operate (i.e. position coaches, coordinators, trainers) but each has just one head coach as shown by the one to one relationship between the coach and program entities. Coaches have a name, a salary, and a title of their position.

Each team plays in multiple games in a year and each game has two teams. The weak entity linking the many to many relationship between team and game is the team_game entity which stores each team’s individual score in the specific game. The team_game entity also has a 1 to 1 relationship to team which shows the opponent of the team in that game.

Because of the transfer portal, players can now be on multiple teams over the time of their collegiate career but only one team per season. The playerYear entity links many players to many teams and vice versa, storing the date they joined and left the team if applicable. The playerYear entity stores information that is pertainent to a player fro a given year but may change next year such as the team tehy are on, their number, or even their height and weight.

The player table stores personal information for each player that likely won't change year over year such as their name, birthdate, contact information, and position. A player can be a mentor of another player (or several other players). This is shown by the 1 to many recursive relationship within the player entity.

A player plays in many games and a game has many players involved. The weak entity between these two entities is gameStats which stores the offensive yardage statistics each player records in each game they play. Passing yards, receiving yards, and rushing yards for each player are stored here.

A player can also now have many NIL deals with several companies. One company (stored in the Sponsor table) also has the ability to sponsor many players. A sponsor has a company name and a unique id. To link the many to many relationship between Sponsor and player there is the NIL table. The NIL table stores the id of the deal as well as the agreed upon dollar amount for the contract between a company and a player.

Our data model stores a range of data regarding college football over several seasons which could be useful for a school administration, third party company interested in sponsoring athletes, or the everyday college football fan!


![Project 2 Diagram final](https://github.com/user-attachments/assets/dd5b17b6-ad1c-4e2d-9c5f-850c42edb2bd)


## Data Dictionary:
![Screenshot (103)](https://github.com/user-attachments/assets/d488680b-b98c-4ab9-80ef-b6e8ca6fea76)


![Screenshot (104)](https://github.com/user-attachments/assets/c9c65e87-58d3-4e88-99f1-471eb9c3858d)


![Screenshot (106)](https://github.com/user-attachments/assets/fa905a5c-ec0a-4979-bb74-92e29149c2f5)


![Screenshot (107)](https://github.com/user-attachments/assets/9f9afbae-150d-4f78-9ce8-c9472e533976)


![Screenshot (108)](https://github.com/user-attachments/assets/129d9386-288d-4039-bb36-10a121da0af6)


![Screenshot (111)](https://github.com/user-attachments/assets/e6ebfb92-4a5c-429a-960d-63a1683508e6)


![Screenshot (113)](https://github.com/user-attachments/assets/c927be2f-b171-4760-9328-37352f939c3c)


![Screenshot 2024-12-01 162828](https://github.com/user-attachments/assets/3d7c46c6-9fd0-4384-8afb-d1059401d28a)


![Screenshot 2024-12-01 164142](https://github.com/user-attachments/assets/cabf376c-ccc1-4361-9f36-95d5a9598c90)


![Screenshot 2024-12-01 165152](https://github.com/user-attachments/assets/a9d55a3a-5a11-4789-a51f-ed64f2f3b414)


![Screenshot 2024-12-01 172002](https://github.com/user-attachments/assets/043bea59-46cd-4ccf-97c7-148ff0e403a2)


![Screenshot 2024-12-01 170604](https://github.com/user-attachments/assets/9a817678-e92f-48b8-b570-c216411d9e80)


![Screenshot 2024-12-01 170835](https://github.com/user-attachments/assets/d96867dc-c40b-442b-8149-debe6eb02594)


## Query Type Matrix:





## Queries:

<img width="491" alt="Screenshot 2024-12-01 at 6 22 51 PM" src="https://github.com/user-attachments/assets/dfce2985-4e56-46ad-89f6-ff8fd9774203">


## Visualzations:





## Database information:

Name of the database: cs_aww39979

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: 
CALL TP_Q1();
