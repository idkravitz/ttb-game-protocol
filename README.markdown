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
        "username": "&lt;username&gt;",
        "password": "&lt;password&gt;"
    }
### Answer ######
    {
        "status": "ok",
        "sid": "&lt;sid&gt;"
    }

## Logout ##

### Request ######
    {
        "cmd": "unregister",
        "sid": "&lt;sid&gt;"
    }
### Answer ######
    {
        "status": "ok"
    }

## Chat ##
### Request ######
    {
        "cmd": "chat",
        "sid": "&lt;sid&gt;",
        "message": "&lt;text&gt;"
    }
### Answer ######
    {
        "status": "ok",
        "chat message": "&lt;message&gt;"
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
        "sid": "&lt;sid&gt;"
    }
### Answer ######
    {
        "status": "ok",
        "games": [ { "username": "&lt;username&gt;" }, ...  ]
    }

## Getting a list of players ##

### Request ######
    {
        "cmd": "getPlayersList",
        "sid": "&lt;sid&gt;"
    }
### Answer ######
    {
        "status": "ok",
        "players": [ { "username": "&lt;username&gt;" }, ...  ]
    }

## Getting an archive of messages ##

### Request ######
    {
        "cmd": "getChartList",
        "sid": "&lt;sid&gt;"
    }
### Answer ######
    {
        "status": "ok",
        "chat":  [ { "username": "&lt;username&gt;",
                     "message": "&lt;message&gt;",
                     "time": "UTC" }, ... ]
    }

## Setting player status ##

### Request ######
    {
        "cmd": "setPlayerStatus",
        "sid": "&lt;sid&gt;",
        "status": "&lt;status&gt;"
    }
### Answer ######
    {
        "status": "ok"
    }

## Creation of a game ##

### Request ######
    {
        "cmd": "createGame",
        "sid": "&lt;sid&gt;",
        "username": "&lt;username&gt;"
    }
### Answer ######
    {
        "status": "ok"
    }

## Join a game ##

### Request ######
    {
        "cmd": "joinGame",
        "sid": "&lt;sid&gt;",
        "username": "&lt;username&gt;"
    }
### Answer ######
    {
        "status": "ok"
    }

## Leaving a game ##

### Request ######
    {
        "cmd": "leaveGame",
        "sid": "&lt;sid&gt;",
        "username": "&lt;username&gt;"
    }
### Answer ######
    {
        "status": "ok"
    }

Tests format specification
==========================
Each test is a file with .tst extension. The name of a test
must contain only Latin letters, symbol "_", and digits. In
other words it must match following regexp /[a-zA-Z0-9_]+\.tst/ 
