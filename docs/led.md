<!--remove-start-->
# LED Component

Run with:
```bash
node eg/led.js
```
<!--remove-end-->

```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);

  // This will grant access to the led instance
  // from within the REPL that's created when
  // running this program.
  this.repl.inject({
    led: led
  });

  led.blink();
});


```


## Breadboard/Illustration


![docs/breadboard/led-13.png](breadboard/led-13.png)  
[Fritzing diagram: docs/breadboard/led-13.fzz](breadboard/led-13.fzz)
![docs/breadboard/led-resistor.png](breadboard/led-resistor.png)  
[Fritzing diagram: docs/breadboard/led-resistor.fzz](breadboard/led-resistor.fzz)
![docs/breadboard/led-13-galileo.png](breadboard/led-13-galileo.png)  
[Fritzing diagram: docs/breadboard/led-13-galileo.fzz](breadboard/led-13-galileo.fzz)
![docs/breadboard/led-13-edison-arduinoboard.png](breadboard/led-13-edison-arduinoboard.png)  
[Fritzing diagram: docs/breadboard/led-13-edison-arduinoboard.fzz](breadboard/led-13-edison-arduinoboard.fzz)
![docs/breadboard/led-13-mega.png](breadboard/led-13-mega.png)  
[Fritzing diagram: docs/breadboard/led-13-mega.fzz](breadboard/led-13-mega.fzz)

This script will make `led` available in the REPL, by default on pin 13.
Now you can try, e.g.:

```js
>> led.stop() // to stop blinking
// then
>> led.off()  // to shut it off (stop doesn't mean "off")
// then
>> led.on()   // to turn on, but not blink
```



<!--remove-start-->
## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
<!--remove-end-->
