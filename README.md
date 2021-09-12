# aweme-crawler-reference

抖音数据抓取研究参考

## 更新 抖音已经上线功能齐全的web版：[抖音web版](https://www.douyin.com/?stay=1)

数据抓取变得方便了

## 利用web页面页接口

- token的生成: [fuck-dytk.js](./fuck-dytk.js)
- web页面数字字体对照关系: [iconfont.py](./iconfont.py)

- 优点
- 缺点

## 真机/模拟器点击配合中间人攻击

- [uiautomator2](https://github.com/openatx/uiautomator2)
- [mitmproxy](https://github.com/mitmproxy/mitmproxy)

### 可以利用url_scheme实现页面跳转和定位

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

### frida hook

```bash
wget -O frida-server.xz https://github.com/frida/frida/releases/download/12.8.13/frida-server-12.8.13-android-x86.xz
xz -d frida-server.xz

adb root
adb push frida-server /data/local/tmp/
adb shell "chmod 755 /data/local/tmp/frida-server"
adb shell "/data/local/tmp/frida-server -l 0.0.0.0"
```

```javascript
rpc.exports = {
    // TODO hook script
};
```

### 模拟器

- [Genymotion](https://www.genymotion.com/)

    `Genymotion` 基于 `VirtualBox` 可以实现跨平台使用, 加上 `Genymotion_ARM_Translation` 的加持完美支持 `ARM`, 个人版本可免费使用。

    - https://www.genymotion.com/download/
    - https://docs.genymotion.com/desktop/3.0/
    - https://github.com/m9rco/Genymotion_ARM_Translation

- arm support
- remote access


## 实现参考

- [maguowei/aweme-sign](https://github.com/maguowei/aweme-sign) Genymotion + frida hook + frp + restful
- [maguowei/appium-douyin](https://github.com/maguowei/appium-douyin) appium & mitmproxy
- [maguowei/app-crawler](https://github.com/maguowei/app-crawler)  uiautomator2 & URL_SCHEMA & mitmproxy
