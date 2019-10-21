TOPIC: jQuery

# jQuery

**jQuery** 是专注于简化 DOM 操作，AJAX 调用和 Event 处理的 JavaScript 库。它被 JavaScript 开发者频繁使用。

jQuery 使用 `$(selector).action()` 的格式给一个（或多个）元素绑定事件。具体来说，`$(selector)` 调用 jQuery 函数选择 `selector` 元素，
并给它绑定一个叫 `.action` 的事件 API。

```javascript
$(document).ready(function(){
  alert("Hello World!");
  $("#blackBox").hide();
});
```

上述代码和以下代码功能相同：

```javascript
window.onload = function() {
  alert( "Hello World!" );
  document.getElementById("blackBox").style.display = "none";
};
```

## 下载 jQuery

| npm | bower (solo file) | Google CDN |
| -- | -- | -- |
| `npm` `install jquery` | `bower install https://code.jquery.com/jquery-3.2.1.min.js` | `https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js` |
