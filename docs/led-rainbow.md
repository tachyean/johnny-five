<!--remove-start-->
# LED - Rainbow

Run with:
```bash
node eg/led-rainbow.js
```
<!--remove-end-->

```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var rgb = new five.Led.RGB([6, 5, 3]);
  var rainbow = ["FF000", "FF7F00", "00FF00", "FFFF00", "0000FF", "4B0082", "8F00FF"];
  var index = 0;

  setInterval(function() {
    if (index + 1 === rainbow.length) {
      index = 0;
    }
    rgb.color(rainbow[index++]);
  }, 500);
});

```


## Breadboard/Illustration


![docs/breadboard/led-rainbow.png](breadboard/led-rainbow.png)  
[Fritzing diagram: docs/breadboard/led-rainbow.fzz](breadboard/led-rainbow.fzz)




<!--remove-start-->
## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
<!--remove-end-->
