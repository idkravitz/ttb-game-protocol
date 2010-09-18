Protocol Description
====================
## Types of server respond ##

#### OK ####
<pre><code>{
    "status": "ok",
    ...
}</code></pre>
#### Bad Request ####
<pre><code>{
    "status": "badRequest",
    ...
}</code></pre>
#### Bad Command ####
<pre><code>{
    "status": "badCommand",
    ...
}</code></pre>
#### Internal Error ####
<pre><code>{
    "status": "internalError",
    ...
}</code></pre>
## Registration ##

### Request ######
<pre><code>{
    "cmd": "register",
    "username": "&lt;username&gt;",
    "password": "&lt;password&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok",
    "sid": "&lt;sid&gt;"
}</code></pre>

## Logout ##

### Request ######
<pre><code>{
    "cmd": "unregister",
    "sid": "&lt;sid&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>

## Chat ##
### Request ######
<pre><code>{
    "cmd": "chat",
    "sid": "&lt;sid&gt;",
    "message": "&lt;text&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok",
    "chat message": "&lt;message&gt;"
}</code></pre>

## Database cleanup ##
### Request ######
<pre><code>{
    "cmd": "clear"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>

## Getting a list of games ##

### Request ######
<pre><code>{
    "cmd": "getGamesList",
    "sid": "&lt;sid&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok",
    "games": [ { "username": "&lt;username&gt;" }, ...  ]
}</code></pre>

## Getting a list of players ##

### Request ######
<pre><code>{
    "cmd": "getPlayersList",
    "sid": "&lt;sid&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok",
    "players": [ { "username": "&lt;username&gt;" }, ...  ]
}</code></pre>

## Getting an archive of messages ##

### Request ######
<pre><code>{
    "cmd": "getChartList",
    "sid": "&lt;sid&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok",
    "chat":  [ { "username": "&lt;username&gt;",
                 "message": "&lt;message&gt;",
                 "time": "UTC" }, ... ]
}</code></pre>

## Setting player status ##

### Request ######
<pre><code>{
    "cmd": "setPlayerStatus",
    "sid": "&lt;sid&gt;",
    "status": "&lt;status&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>

## Creation of a game ##

### Request ######
<pre><code>{
    "cmd": "createGame",
    "sid": "&lt;sid&gt;",
    "username": "&lt;username&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>

## Join a game ##

### Request ######
<pre><code>{
    "cmd": "joinGame",
    "sid": "&lt;sid&gt;",
    "username": "&lt;username&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>

## Leaving a game ##

### Request ######
<pre><code>{
    "cmd": "leaveGame",
    "sid": "&lt;sid&gt;",
    "username": "&lt;username&gt;"
}</code></pre>
### Answer ######
<pre><code>{
    "message": "ok"
}</code></pre>
