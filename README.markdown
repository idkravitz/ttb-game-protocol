Описание протокола
==================
## Pегистрация ##

### Запрос ######
<pre><code>{
    'cmd': 'register',
    'username': '&lt;username&gt;',
    'password': '&lt;password&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok',
    'sid': '&lt;sid&gt;'
}</code></pre>

## Разрегистрация ##

### Запрос ######
<pre><code>{
    'cmd': 'unregister',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok'
}</code></pre>

## Чат ##
### Запрос ######
<pre><code>{
    'cmd': 'chat',
    'sid': '&lt;sid&gt;',
    'message': '&lt;text&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok',
    'chat message': '&lt;message&gt;'
}</code></pre>

## Очистка базы данных ##
### Запрос ######
<pre><code>{
    'cmd': 'clear'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok'
}</code></pre>

## Получение списка игр ##

### Запрос ######
<pre><code>{
    'cmd': 'getGameList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok',
    'games': [ { 'username': '&lt;username&gt;' }, ...  ]
}</code></pre>

## Получение списка игроков ##

### Запрос ######
<pre><code>{
    'cmd': 'getPlayersList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok',
    'players': [ { 'username': '&lt;username&gt;' }, ...  ]
}</code></pre>

## Получение архива сообщений ##

### Запрос ######
<pre><code>{
    'cmd': 'getChartList',
    'sid': '&lt;sid&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'message': 'ok',
    'chat':  [ { 'username': '&lt;username&gt;',
                 'message': '&lt;message&gt;',
                 'time': 'UTC' }, ... ]
}</code></pre>

