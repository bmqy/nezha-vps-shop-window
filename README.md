# VPS橱窗

一个简单的哪吒面板主题。

## 部署

### Cloudflare Pages (推荐)

#### 环境变量

`NEZHA_DASHBOARD_DOMAIN` 填写你的哪吒面板域名。

## 自定义

### 个性化配置

```js
<script lang="json" rel="preferences">
{
    // 自定义背景图
    "customBackgroundImage": "https://api.timelessq.com/bing/random",
    // 自定义logo
    "customLogo": "https://image.bmqy.net/wp-content/uploads/2018/09/logo-1.png",
    // 自定义标题
    "customTitle": "VPS橱窗",
    // 自定义描述
    "customDesc": "VPS Shop Window",
    // 应用主题
    "customTheme": "rose",
    // 语言：zh-CN、en，默认zh-CN
    "customLanguage": "zh-CN",
    // 是否启用半透明
    "useSemitransparent": true,
    // 自定义导航链接
    "customNavLinks": [
        {
            "link": "https://t.me/bmqyChatBot",
            "name": "Telegram ",
            "svg": "%3Csvg%20t%3D%221736211069166%22%20class%3D%22icon%22%20viewBox%3D%220%200%201024%201024%22%20version%3D%221.1%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20p-id%3D%221889%22%20width%3D%2220%22%20height%3D%2220%22%3E%3Cpath%20d%3D%22M512%2016C238%2016%2016%20238%2016%20512s222%20496%20496%20496%20496-222%20496-496S786%2016%20512%2016z%20m243.6%20339.8l-81.4%20383.6c-6%2027.2-22.2%2033.8-44.8%2021l-124-91.4-59.8%2057.6c-6.6%206.6-12.2%2012.2-25%2012.2l8.8-126.2%20229.8-207.6c10-8.8-2.2-13.8-15.4-5l-284%20178.8-122.4-38.2c-26.6-8.4-27.2-26.6%205.6-39.4l478.2-184.4c22.2-8%2041.6%205.4%2034.4%2039z%22%20p-id%3D%221890%22%20fill%3D%22%231296db%22%3E%3C%2Fpath%3E%3C%2Fsvg%3E"
        },
        {
            "link": "https://wpa.qq.com/msgrd?V=3&Uin=88268459&Site=nezha.887776.xyz&menu=yes",
            "name": "QQ",
            "svg": "%3Csvg%20t%3D%221736210934546%22%20class%3D%22icon%22%20viewBox%3D%220%200%201024%201024%22%20version%3D%221.1%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20p-id%3D%221544%22%20width%3D%2220%22%20height%3D%2220%22%3E%3Cpath%20d%3D%22M933.446%20643.862c-18.784-108.945-97.673-180.323-97.673-180.323%2011.268-98.92-30.056-116.461-30.056-116.461-8.701-306.05-272.335-300.692-277.87-300.546-5.542-0.146-269.211-5.505-277.872%20300.548%200%200-41.325%2017.54-30.055%20116.461%200%200-78.895%2071.378-97.676%20180.323%200%200-10.034%20184.083%2090.16%2022.544%200%200%2022.544%2061.344%2063.867%20116.455%200%200-73.897%2025.062-67.621%2090.165%200%200-2.518%2072.618%20157.784%2067.625%200%200%20112.702-8.757%20146.516-56.35h29.795c33.809%2047.595%20146.514%2056.35%20146.514%2056.35%20160.262%204.993%20157.781-67.625%20157.781-67.625%206.238-65.103-67.62-90.165-67.62-90.165%2041.324-55.11%2063.862-116.455%2063.862-116.455%20100.156%20161.537%2090.164-22.546%2090.164-22.546z%22%20fill%3D%22%231fb6ff%22%20p-id%3D%221545%22%3E%3C%2Fpath%3E%3C%2Fsvg%3E"
        },
        {
            "link": "mailto:notice@bmqy.net",
            "name": "Email",
            "svg": "%3Csvg%20t%3D%221736211091357%22%20class%3D%22icon%22%20viewBox%3D%220%200%201024%201024%22%20version%3D%221.1%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20p-id%3D%222142%22%20width%3D%2220%22%20height%3D%2220%22%3E%3Cpath%20d%3D%22M926.47619%20355.644952V780.190476a73.142857%2073.142857%200%200%201-73.142857%2073.142857H170.666667a73.142857%2073.142857%200%200%201-73.142857-73.142857V355.644952l304.103619%20257.828572a170.666667%20170.666667%200%200%200%20220.745142%200L926.47619%20355.644952zM853.333333%20170.666667a74.044952%2074.044952%200%200%201%2026.087619%204.778666%2072.704%2072.704%200%200%201%2030.622477%2022.186667%2073.508571%2073.508571%200%200%201%2010.678857%2017.67619c3.169524%207.509333%205.12%2015.652571%205.607619%2024.210286L926.47619%20243.809524v24.380952L559.469714%20581.241905a73.142857%2073.142857%200%200%201-91.306666%202.901333l-3.632762-2.925714L97.52381%20268.190476v-24.380952a72.899048%2072.899048%200%200%201%2040.155428-65.292191A72.97219%2072.97219%200%200%201%20170.666667%20170.666667h682.666666z%22%20p-id%3D%222143%22%20fill%3D%22%23f3A73F%22%3E%3C%2Fpath%3E%3C%2Fsvg%3E"
        }
    ]
}
</script>
```

### 加载第三方脚本和样式表资源

```js
<script lang="json" rel="resource">
  [ "https://cdn.jsdelivr.net/gh/mocchen/cssmeihua/js/aixin.js",
  "https://cdn.jsdelivr.net/gh/mocchen/cssmeihua/js/yinghua.js" ]
</script>
```

### 加载脚本代码

```js
<script>console.log("Hello World");</script>
```

### 加载样式代码

```js
<style>
body{
  background-color: #fff;
}
</style>
```

## 联系作者

[@chanel](https://t.me/tcbmqy)

[@group](https://t.me/tgbmqy)
