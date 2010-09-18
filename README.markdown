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
    'ok',
    '&lt;number&gt;'
}</code></pre>

## Разрегистрация ##

### Запрос ######
<pre><code>{
    'cmd': 'unregister',
    'sid': '&lt;number&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'ok'
}</code></pre>

## Pегистрация ##

### Запрос ######
<pre><code>{
    'cmd': 'chat',
    'sid': '&lt;number&gt;',
    'message': '&lt;text&gt;'
}</code></pre>
### Ответ ######
<pre><code>{
    'ok',
    '&lt;message&gt;'
}</code></pre>


