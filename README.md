# GL_Game
JL_Game_Challenge
Framework: dotnet core 6 web api
Local URL : https://localhost:7000/
Swagger test URL: https://localhost:7000/swagger/index.html

---------------------------------------------------------------------------------------
Game:
Used to get,create,update,Edit and delete a game
Get:
https://localhost:7000/api/Games
Get by id :
https://localhost:7000/api/Games/id

Post:
Used to add new game
https://localhost:7000/api/Games
body form:
{
  "name": "string",
  "genre": "string"
}

PUT:
Update a game
https://localhost:7000/api/Games/id
	
body form:
{
  "name": "string",
  "genre": "string"
}

Delete :
https://localhost:7000/api/Games/id



---------------------------------------------------------------------------------------

Plateforms:
 
Used to get,create,update,Edit and delete a plateform
Get:
https://localhost:7000/api/Platforms

Get by id
https://localhost:7000/api/Platforms/id

Post:
https://localhost:7000/api/Platforms

body form:
{
  "name": "string"
}

Put:
https://localhost:7000/api/Platforms/id
body form:
{
  "name": "string"
}

Delete:
https://localhost:7000/api/Platforms/id

---------------------------------------------------------------------------------------
PlateformGames:
Used to create,delete and get games under a plateform
 
GET:
https://localhost:7000/api/PlateformGames

GET by id:
https://localhost:7000/api/PlateformGames/id

Post :
Used to add a game under a plateform
https://localhost:7000/api/PlateformGames

body form:
{
  "gameId": number,
  "platformId": number
}

Delete:
Used to cancel a game under a plateform
https://localhost:7000/api/PlateformGames/id

---------------------------------------------------------------------------------------
User :
 Used to get,create,update,Edit and delete a user
 
Get:
https://localhost:7000/api/Users

Get by id :
https://localhost:7000/api/Users/id

Post:
https://localhost:7000/api/Users
body form:
{
  "name": "string"
}


Put:
https://localhost:7000/api/Users/id
body form:
{
  "name": "string"
}
Delete:
https://localhost:7000/api/Users/id


---------------------------------------------------------------------------------------

UserGames:
Used to add,get and delete a players and total play time for a game
 
Get:
https://localhost:7000/api/UserGames
Get by id :
https://localhost:7000/api/UserGames/id

Post:

Create relation between user and game and initialize play time using a existing relation will add a new play time to old total play time
https://localhost:7000/api/UserGames

Body form:
   {
    "gameId": number,
    "userId": number,
    "totalPlayTime": number,
    }

Delete:
https://localhost:7000/api/UserGames/id






---------------------------------------------------------------------------------------


JL_Game:
 
Get data:
https://localhost:7000/api/JL_Game

To serve initial data like :
[
  {
    "userId": 8,
    "game": "League of legends",
    "playTime": 500,
    "genre": "MOBA",
    "platforms": [
      "PC"
    ]
  },
  {
    "userId": 7,
    "game": "World of warcraft",
    "playTime": 1500,
    "genre": "MMORPG",
    "platforms": [
      "PC"
    ]
  },
  {
    "userId": 1,
    "game": "The last of us 2",
    "playTime": 100,
    "genre": "FPS",
    "platforms": [
      "PS4",
      "PC"
    ]
  },
  {
    "userId": 7,
    "game": "Hearthstone",
    "playTime": 1000,
    "genre": "Card Game",
    "platforms": [
      "PC"
    ]
  },
  {
    "userId": 7,
    "game": "FIFA 2020",
    "playTime": 2000,
    "genre": "Sport",
    "platforms": [
      "PC",
      "PS4",
      "XBOX"
    ]
  },
  {
    "userId": 2,
    "game": "Among Us",
    "playTime": 5000,
    "genre": "Multiplayer",
    "platforms": [
      "PC",
      "Android"
    ]
  },
  {
    "userId": 2,
    "game": "Valorant",
    "playTime": 4000,
    "genre": "FPS",
    "platforms": [
      "PC"
    ]
  }
]


Select_top_by_playtime:
To get the top played game by total players play time
 can be used without options. 
https://localhost:7000/api/JL_Game/select_top_by_playtime

Result:
 
Can be used with only genre option:

https://localhost:7000/api/JL_Game/select_top_by_playtime?genre=FPS


 

Can be used with only plateform option:
https://localhost:7000/api/JL_Game/select_top_by_playtime?platforms=PS4




 

Can be used with both options genre and plateform
https://localhost:7000/api/JL_Game/select_top_by_playtime?genre=FPS&platforms=PC

 


Select_top_by_players:
To get the top played game by players number 

can be used without options. 
https://localhost:7000/api/JL_Game/select_top_by_players

 
Can be used with only genre option:
https://localhost:7000/api/JL_Game/select_top_by_players?genre=FPS


 

Can be used with only platform option:
https://localhost:7000/api/JL_Game/select_top_by_players?platforms=PS4


 

Can be used with both options genre and plateform
https://localhost:7000/api/JL_Game/select_top_by_players?genre=FPS&platforms=PC


 
