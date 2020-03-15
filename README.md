# aweme-crawler-reference

抖音数据抓取研究参考

## 利用web页面页接口

- 优点
- 缺点

## 真机/模拟器点击配合中间人攻击

- 可以利用url_scheme实现页面跳转和定位

部分常用的跳转协议

```python
URL_SCHEMA_MAP = {
    'home': "snssdk1128://feed?refer=web",
    'user': 'snssdk1128://user/profile/{uid}?refer=web',
    'detail': 'snssdk1128://aweme/detail/{aweme_id}?refer=web',
    'challenge': 'snssdk1128://challenge/detail/{challenge_id}?refer=web',
    'music': 'snssdk1128://music/detail/{music_id}?refer=web',
    'live': 'snssdk1128://live?room_id={room_id}&user_id={user_id}&from=webview&refer=web',
    'poi":': 'snssdk1128://poi/?id={poi_id}',
    'webview': 'snssdk1128://webview?url={url}&from=webview&refer=web',
    'webview_fullscreen': 'snssdk1128://webview?url={url}&from=webview&hide_nav_bar=1&refer=web',
    'poidetail': 'snssdk1128://poi/detail?id={id}&from=webview&refer=web',
    'forward': 'snssdk1128://forward/detail/{id}',
    'billboard_word': 'snssdk1128://search/trending',
    'billboard_video': "snssdk1128://search/trending?type=1",
    'billboard_music': "snssdk1128://search/trending?type=2",
    'billboard_positive': "snssdk1128://search/trending?type=3",
    'billboard_star': "snssdk1128://search/trending?type=4",
}
```

## 特殊的漏洞/后门

## hook so 库签名方法, 封装api service 调用

TODO
