# anto-danmu
超级简单的自动发弹幕脚本


## 使用方法
- 打开直播页面按F12
- 将下方的代码复制粘贴进去**按回车**
- 输入start()开始自动发弹幕

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


