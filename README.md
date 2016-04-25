### Popup弹出层
+ 格式
```
    <div id="mask" class="mask"></div>
    <div class="hero-get-area">
        <h2 class="hero-title">您的运气不错，采集黄金星辰后发现：</h2>
        <div class="hero-you-get">
            <div class="close"><img src="img/close.png" alt="" width="50px" height="50px"></div>
            <div class="hero-pic"><img src="img/2_64003.jpg" alt="">
                <div class="cover"></div>
            </div>
            <h3 class="hero-name">皮肤 龙的传人 李青</h3>
            <div class="operation">
                <button class="comfirm">确定</button>
                <button class="share">立即分享</button>
            </div>
        </div>
    </div>
```
+ 参数
    + type，抽奖的种类，"黄金星辰" or "钻石星辰"
    + number，多少个
    + ic_src，图片路径"
    + kind，"皮肤 ",还是"英雄"
    + kind_name: "名称"

    例如:
    ```
        Popup.alert(function(e) {}, {
            type: "黄金星辰",
            number: "1个",
            pic_src: "img/2_64003.jpg",
            kind: "皮肤 ",
            kind_name: "龙的传人 李青"
        })
    ```

+ 功能
    + alert
    + comfirm(continue ...)
    + ...
    + ...
    + ...

### 注册一个对象到window上

```
if (typeof module != 'undefined' && module.exports) {
        module.exports = Popup;
    } else if (typeof define === 'function' && define.amd) {
        define('Popup', [], function() {
            return Popup;
        });
    } else {
        this.Popup = Popup;//把封装的好的对象注册到window上
    }
```