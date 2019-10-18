TOPIC: JQuery
AUTHORS: Emanuel; github@vecr.me; github:vecr25
         Fuqiao Xue; xfq@mozilla.net; mdn:xfq
         Farouk Charkas; faroukcharkas@mozilla.net; mdn:faroukcharkas
         Shaun Kelly; 6stringbeliever@mozilla.net; mdn:6stringbeliever

# JQuery

**jQuery** is a JavaScript **Library** that focuses on simplifying DOM manipulation,
AJAX calls, and Event handling. It is used by JavaScript developers frequently.

jQuery uses a format, `$(selector).action()` to assign an element(s) to an event. To explain it in
detail, `$(selector)` will call jQuery to select `selector` element(s), and assign it to an event
API called `.action()`.

```javascript
$(document).ready(function(){
  alert("Hello World!");
  $("#blackBox").hide();
});
```

The above code carries out the same function as the following code:

```javascript
window.onload = function() {
  alert( "Hello World!" );
  document.getElementById("blackBox").style.display = "none";
};
```

## Download jQuery

| npm | bower (solo file) | Google CDN |
| -- | -- | -- |
| `npm` `install jquery` | `bower install https://code.jquery.com/jquery-3.2.1.min.js` | `https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js` |

## Learn More

### General Knowledge

- [jQuery](https://en.wikipedia.org/wiki/jQuery) on Wikipedia
- [jQuery Official Website](https://jquery.com/)

### Technical information

- [API reference documentation](https://api.jquery.com/)
