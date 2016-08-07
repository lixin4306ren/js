# DOM EventListener

`addEventListener()` 方法用于向指定元素添加事件句柄。  
`addEventListener()` 方法添加的事件句柄不会覆盖已存在的事件句柄。你可以向一个元素添加多个事件句柄。  
你可以向同个元素添加多个同类型的事件句柄，如：两个 "click" 事件。  
你可以向任何 DOM 对象添加事件监听，不仅仅是 HTML 元素。如： window 对象。  
```
<script>
window.addEventListener("resize", function(){
    document.getElementById("demo").innerHTML = Math.random();
});
</script>
```

`addEventListener()` 方法可以更简单的控制事件（冒泡与捕获）。
当你使用 `addEventListener()` 方法时, JavaScript 从 HTML 标记中分离开来，可读性更强， 在没有控制HTML标记时也可以添加事件监听。  

在用户点击按钮时触发监听事件：
```
document.getElementById("myBtn").addEventListener("click", displayDate);
```


你可以使用 `removeEventListener()` 方法来移除事件的监听。


