#POST /favorites/create

收藏消息(当前用户关注者和未设置隐私用户发出的消息)

##路径

    http://api.fanfou.com/statuses/favorites/create/id.[json|xml|rss]

##调用方法

    POST 

##参数：

###id

- 作用: 目标消息的id

- 格式: `http://api.fanfou.com/statuses/favorites/create/id.[json|xml|rss]`

- 字段说明: 必选

###mode

- 作用: 当`mode=default`(默认)时,返回消息中用户信息包含用户自定义profile

- 格式: `mode=mode_str`

- 字段说明: 可选

###format

- 作用: 当`format=html`时,返回消息中@提到的用户,网址等输出html链接

- 格式: `format=html`

- 字段说明: 可选

###callback

- 格式: callback=javascript函数名

- 作用: 当使用json格式时,生成的json对象将作为参数传给指定的javascript函数

- 字段说明: 可选

##返回结果

###成功

返回被收藏消息的详细内容

- HTTP Status Code

    `200 OK HTTP/1.1`

- 返回值

    * json格式

    被收藏消息的详细内容，消息格式参见[[status show]](/statuses/show)