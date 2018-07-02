# auto-danmu
超级简单的自动发弹幕脚本

![图片](https://github.com/xiongyizhu/auto-danmu/blob/master/image/danmu.gif)

## 使用说明
- 打开直播页面按F12
- 将下方的代码复制粘贴到控制台**按回车**
- 输入start()**按回车**开始自动发弹幕
- 输入stop()**按回车**停止自动发弹幕

## 大家一起玩
- <a target="_blank" href="http//shang.qq.com/wpa/qunwpa?idkey=974f2dee6d684148de65f6bb0b5bbabfdc3eec47ddbc7f971a4b33ef08178c03"><img border="0" src="http://pub.idqqimg.com/wpa/images/group.png" alt="自动弹幕群" title="自动弹幕群"></a>
 一起进入同一个直播间同时运行自动弹幕

![图片](https://github.com/xiongyizhu/auto-danmu/blob/master/image/qun.png)

## 斗鱼TV代码
```
const area = document.getElementsByClassName('cs-textarea')[0]
const btn = document.getElementsByClassName('b-btn')[0]

const danmu = '哈哈哈哈，主播好搞笑'
let i = 0
let interval
function start () {
  interval = setInterval(function () {
    area.value = danmu + i
    if (btn.innerHTML === '发送') {
      btn.click()
      i++
    }
  }, 1000)
}

function stop () {
  clearInterval(interval)
}
```
#### 后面加数字太容易被禁言了，那就加随机字母吧
```
const area = document.getElementsByClassName('cs-textarea')[0]
const btn = document.getElementsByClassName('b-btn')[0]

const danmu = '哈哈哈哈，主播好搞笑'
let interval
function start () {
  interval = setInterval(function () {
	let ranNum = Math.ceil(Math.random() * 25);
    area.value = danmu + String.fromCharCode(65+ranNum)
    if (btn.innerHTML === '发送') {
      btn.click()
    }
  }, 1000)
}

function stop () {
  clearInterval(interval)
}
```

## 熊猫TV代码
```
const area = document.getElementsByClassName('room-chat-texta')[0]
const btn = document.getElementsByClassName('room-chat-send ')[0]

const danmu = '哈哈哈哈，主播好搞笑'
let i = 0
let interval
function start () {
  interval = setInterval(function () {
    area.value = danmu + i
    if (btn.innerHTML === '发送') {
      btn.click()
      i++
    }
  }, 1000)
}

function stop () {
  clearInterval(interval)
}
```

## 虎牙TV代码
```
const area = document.getElementById('pub_msg_input')
const btn = document.getElementById('msg_send_bt')

const danmu = '哈哈哈哈，主播好搞笑'
let i = 0
let interval
function start () {
  interval = setInterval(function () {
    area.value = danmu + i
    let time=document.getElementsByClassName("msg_send_time")
    if (time[0]==undefined || time[0].innerHTML==0) {
      btn.setAttribute("class", "btn-sendMsg hiido_stat enable"); 
      btn.click()
      i++
    }
  }, 1000)
}

function stop () {
  clearInterval(interval)
}
```

## 全民TV代码
```
const area = document.getElementsByClassName('room_w-sender_textarea')[0]
const btn = document.getElementsByClassName('room_w-sender_submit-btn')[0]

const danmu = '哈哈哈哈，主播好搞笑'
let i = 0
let interval
function start () {
  interval = setInterval(function () {
    area.value = danmu + i
    if (btn.innerHTML === '发送') {
      btn.click()
      i++
    }
  }, 1000)
}

function stop () {
  clearInterval(interval)
}
```


#### Tips：

###### 建议：不要发广告，发广告会被封禁账号

###### 时效性：可能过一段时间直播平台就河蟹了

###### 免责申明：使用该代码造成任何违法行为均由使用者自行承担
