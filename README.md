# Simple-live-rolling-song-list

---

一个简单的直播滚动歌单，在OBS，哔哩哔哩直播姬等直播软件中可以以浏览器的方式嵌入直播画面



# 食用方式



## 修改参数

打开`cfg.json`文件（可以用`记事本`等工具打开）

在这个文件里面添加歌曲，修改字体颜色等

```js
// 歌单字体大小，请在等号后面填入整数
var my_font_size = 22

// 歌单字体颜色 修改括号内对应的数值
// rgba( 红色, 绿色, 蓝色, 透明度)   颜色rgb这3个数的取值为 0 <= rgb <= 255     透明度a 的取值为： 0<= 透明度 <= 1
var my_font_color = 'rgba(93, 134, 206, 1)'

// 比如纯白色为：rgba( 255 , 255 , 255 , 1)   半透明的纯白色为：rgba( 255 , 255 , 255 , 0.7)
// 纯黑色为： rgba(0 , 0 , 0 , 1)

// 歌单长度（越长同时显示的歌曲就越多）
var list_height = 260

// 歌单宽度（越宽，歌名较长的歌曲就不用换行显示）
var list_width = 400

// 歌单每隔多少毫秒(ms)向上移动一次
var rolling_timer = 15

// 歌单每次向上移动多少像素
var rolling_speed = 1
```



## 增加，删除歌曲



增加歌曲：复制一行，修改双引号 " " 里面的文字即可

```js

// 歌单列表 
var music_list = [
    "TA",
]
// 复制一行
var music_list = [
    "TA",
    "TA",
]
// 修改歌名
var music_list = [
    "TA",
    "藏进繁星",
]


```



删除歌曲：删除那一行即可

```js
var music_list = [
    "TA",  // 直接删除第一行"TA"
    "安静",
    "故梦",
    "房间",
    "稻香",
]

var music_list = [
    
    "安静",
    "故梦",
    "房间",
    "稻香",
]
```





## 添加到直播画面中



### 以OBS为例

添加 -> 浏览器 -> 勾选本地文件 -> 选择`index.html`



