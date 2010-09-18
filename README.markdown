Protocol description
====================
## Types of server respond ##

#### OK ####
    {
        "status": "ok",
        ...
    }
#### Bad Request ####
    {
        "status": "badRequest",
        "message": "description",
        ...
    }
#### Bad Command ####
    {
        "status": "badCommand",
        "message": "description",
        ...
    }
#### Internal Error ####
    {
        "status": "internalError",
        "message": "description",
        ...
    }
## Registration ##

### Request ######
    {
        "cmd": "register",
        "username": "<username>",
        "password": "<password>"
    }
### Answer ######
    {
        "status": "ok",
        "sid": "<sid>"
    }

## Logout ##

### Request ######
    {
        "cmd": "unregister",
        "sid": "<sid>"
    }
### Answer ######
    {
        "status": "ok"
    }

## Chat ##
### Request ######
    {
        "cmd": "chat",
        "sid": "<sid>",
        "message": "<text>"
    }
### Answer ######
    {
        "status": "ok",
        "chat message": "<message>"
    }

## Database cleanup ##
### Request ######
    {
        "cmd": "clear"
    }
### Answer ######
    {
        "status": "ok"
    }

## Getting a list of games ##

### Request ######
    {
        "cmd": "getGamesList",
        "sid": "<sid>"
    }
### Answer ######
    {
        "status": "ok",
        "games": [ { "username": "<username>" }, ...  ]
    }

## Getting a list of players ##

### Request ######
    {
        "cmd": "getPlayersList",
        "sid": "<sid>"
    }
### Answer ######
    {
        "status": "ok",
        "players": [ { "username": "<username>" }, ...  ]
    }

## Getting an archive of messages ##

### Request ######
    {
        "cmd": "getChartList",
        "sid": "<sid>"
    }
### Answer ######
    {
        "status": "ok",
        "chat":  [ { "username": "<username>",
                     "message": "<message>",
                     "time": "UTC" }, ... ]
    }

## Setting player status ##

### Request ######
    {
        "cmd": "setPlayerStatus",
        "sid": "<sid>",
        "status": "<status>"
    }
### Answer ######
    {
        "status": "ok"
    }

## Creation of a game ##

### Request ######
    {
        "cmd": "createGame",
        "sid": "<sid>",
        "username": "<username>"
    }
### Answer ######
    {
        "status": "ok"
    }

## Join a game ##

### Request ######
    {
        "cmd": "joinGame",
        "sid": "<sid>",
        "username": "<username>"
    }
### Answer ######
    {
        "status": "ok"
    }

## Leaving a game ##

### Request ######
    {
        "cmd": "leaveGame",
        "sid": "<sid>",
        "username": "<username>"
    }
### Answer ######
    {
        "status": "ok"
    }

Tests format specification
==========================
Each test is a file with .tst extension. The name of a test
must contain only Latin letters, symbol "\_", and digits. In
other words it must match following regexp /[a-zA-Z0-9\_]+\\.tst/ 
