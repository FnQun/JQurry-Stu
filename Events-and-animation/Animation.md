### Animation  
#### JQuery 中的动画   
###### 基本动画  
+ 显示和隐藏  
`show() : display: 非[none]状态`  
`hide() : display: none`  
可指定 fast / slow / normal 关键字[__加引号__] 或者 具体的毫秒[__可不加引号__]  
`show("fast")` / `hide(1000)` [毫秒]  
+ 改变透明度  
`fadeIn() / fadeOut()`  
+ 改变高度  
`slideUp() / slideDown()`  

###### 自定义动画  

+ animate()
`animate(params, speed, callback)`  
params : 属性和值 `{ attribute1 : "value", attribute2 : "value",... }`  
speed : 速度参数 [可选]  
callback : 回调函数 [可选]  

+ 动画执行方式(多重动画)  
同时执行  
```
$("div").click(function(){
    $("this").animate({attribute1: "value", attribute2: "value"},fast);
});
```
顺序执行  
```
$("div").click(function(){
    $("this").animate({attribute1: "value"},fast);
    $("this").animate({attribute2: "value"},fast);
    //分开写
});
```
或者
```
$("div").click(function(){
    $("this").animate({attribute1: "value"},fast).animate({attribute2: "value"},fast);
    //链式写法
});
```  

自定义动画综合效果由 
+ __[动画样式分解]__ 
+ __[动画执行分解]__  
*综合而来
