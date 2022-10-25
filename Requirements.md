## Requirements:
<!-- 1. User roles:
   - default
   - moderator
   - admin
---
1. Default user:
   - authentification
   - read the information
2. Moderator:
   - edit and add all stats
3. Admin:
   - same as moderator and block user
--- -->
Database diagram:

![alt text](Pictures/diagram.jpg)
---
Database description:

**Highlighted** fields are primary keys or part of them

<!-- - User - all users
   - **IdUser** - uuid
   - IdRole - uuid(foreign key)
   - Name - text(user name)
   - LastName - text(user last name)
   - Password - text(user password)
   - Email - text(user email)
   - Is_blocked - bool(is the user blocked or not) -->

<!-- - Role - roles for users
   - **IdRole** - uuid
   - Name - text(role name)
- Log - user action logs
   - **IdUser** - uuid(foreign key)
   - Date - time(time of user action)
   - Info - text(user action for log) -->

- Season - football season
   - **idSeason** - serial
   - Championship - serial(id of championship)
   - Cup - serial(id of cup)

- Championship - football championship
   - **idChampionship** - uuid
   - Team - list of teams

- Team - football team
   - **idTeam** - serial
   - Name - varchar(team name)
   - Player - list of players
   - Game - list of games
   - Victory - list of victories
   - Draw - list of draws
   - Lose - list of loses

- Player - football player
   - **idPlayer** - serial
   - Name - varchar(team name)
   - Goal - int(count of goals)
   - Assist - int(count of assists)
   

- Game - football game
   - **idGame** - serial
   - Team 1 - id of the first team
   - Team 2 - id of the second team
   - Score - varchar(match score)
   - isVictory - bool(if first team wins)
   - isDraw(if draw)
   - isLose(if the first team loses)

- Goal
   - **idGoal** - serial
   - idPlayer - id of player

- Assist
   - **idAssist** - serial
   - idPlayer - id of player

- Genre - movie genre
   - **IdGenre** - uuid
   - Name - text(genre name)

- Victory
   - **idVictory** - serial
   - idGame - id of the game
   - idTeam - id of the team
 
- Draw
   - **idDraw** - serial
   - idGame - id of the game
   - idTeam - id of the team
 
- Lose
   - **idLose** - serial
   - idGame - id of the game
   - idTeam - id of the team
---
<!-- Normalized database: -->

<!-- ![alt text](Pictures/normalized.png) -->
