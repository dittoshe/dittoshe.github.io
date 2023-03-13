---
layout: post
title: 防抖和节流
tags: js基础
stickie: true
---

### 防抖debounce
防止抖动，避免事件重复触发，如果短时间内大量触发同一事件，只会执行最后一次。
应用场景：
- 点击事件，用户多次点击导致与服务端频繁交互
- 输入框自动保存事件
- 浏览器resize事件
```
function debounce(fun,wait){
    let timer;
    return (...args)=>{
    	if (timer){
        	clearTimeout(timer);
        }
        timer = setTimeout(()=>{
        	fun(...args);
        },wait)
    }
}
window.onresize = debounce(()=>{
	console.log(1);
},1000);
//页面在频繁resize的时候，控制台也只会打印一次1
```

### 节流throttle
减少流量，控制触发频率，限制一个动作在规定时间内只能执行一次
应用场景：
- scroll 事件，每隔一秒计算一次位置信息等
- input 框实时搜索并发送请求展示下拉列表，每隔一秒发送一次请求
```
function throttle (fn,delay){
    let timer = null
    return ()=>{
        if (timer){return}
        timer = setTimeout(() => {
            fn.apply(this,arguments)
            timer = null
        }, delay);       
    }
}
```

