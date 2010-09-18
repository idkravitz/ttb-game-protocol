Protocol Description
====================
## Registration ##

### Request ######
<pre><code>{
    'cmd': 'register',
    'username': '&lt;username&gt;',
    'password': '&lt;password&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok',
    'sid': '&lt;sid&gt;'
}</code></pre>

## Logout ##

### Request ######
<pre><code>{
    'cmd': 'unregister',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok'
}</code></pre>

## Chat ##
### Request ######
<pre><code>{
    'cmd': 'chat',
    'sid': '&lt;sid&gt;',
    'message': '&lt;text&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok',
    'chat message': '&lt;message&gt;'
}</code></pre>

## Database cleanup ##
### Request ######
<pre><code>{
    'cmd': 'clear'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok'
}</code></pre>

## Getting a list of games ##

### Request ######
<pre><code>{
    'cmd': 'getGamesList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok',
    'games': [ { 'username': '&lt;username&gt;' }, ...  ]
}</code></pre>

## Getting a list of players ##

### Request ######
<pre><code>{
    'cmd': 'getPlayersList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok',
    'players': [ { 'username': '&lt;username&gt;' }, ...  ]
}</code></pre>

## Getting the archive of messages ##

### Request ######
<pre><code>{
    'cmd': 'getChartList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok',
    'chat':  [ { 'username': '&lt;username&gt;',
                 'message': '&lt;message&gt;',
                 'time': 'UTC' }, ... ]
}</code></pre>

## Creation of the game ##

### Request ######
<pre><code>{
    'sid': '&lt;sid&gt;',
    'username': '&lt;username&gt;'
}</code></pre>
### Answer ######
<pre><code>{
    'message': 'ok'
}</code></pre>