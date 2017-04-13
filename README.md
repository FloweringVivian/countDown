# countDown
jquery封装的倒计时插件 倒计时的效果是项目中经常用到的，这款倒计时插件是我根据实际项目中的需求自己封装的，以下请见使用说明
### 使用说明
首先引入两个js文件，一是jquery-1.11.1.min.js，另一个是我自己封装的jquery.Countdown.js

```javascript
<script type="text/javascript" src="js/jquery-1.11.1.min.js"></script>
<script type="text/javascript" src="js/jquery.Countdown.js"></script>
```

html基本布局如下：

```javascript
<!-- 倒计时 start -->
<div class="try_countdown clearfix">
    <div class="try_fl">剩余时间：</div>
    <div id="countdown_dashboard">
        <div class="dash days_dash">                            
            <div class="digit"></div>
            <div class="digit"></div>
            <span class="dash_title">天</span>
        </div>
        <div class="dash hours_dash">                            
            <div class="digit"></div>
            <div class="digit"></div>
            <span class="dash_title">时</span>
        </div>

        <div class="dash minutes_dash">                            
            <div class="digit"></div>
            <div class="digit"></div>
            <span class="dash_title">分</span>
        </div>
        <div class="dash seconds_dash">                            
            <div class="digit"></div>
            <div class="digit"></div>
            <span class="dash_title">秒</span>
        </div>
    </div>
</div>
<!-- 倒计时 end -->
```

使用及配置选项

```javascript
$(function(){
    // 倒计时
    $('#countdown_dashboard').countDown({
        targetDate: {  //目标时间
            'day':      12,   //日
            'month':    5,    //月
            'year':     2017, //年
            'hour':     0,    //时
            'min':      0,    //分
            'sec':      0     //秒                 
        },
        //serverTime: time_server_Date,  //服务器时间
        onComplete: function(){  //倒计时完成后
            alert("倒计时完成");
        }
    });
})
```

调用$('#countdown_dashboard').stopCountDown();可以停止倒计时

调用$('#countdown_dashboard').startCountDown();可以开始倒计时


