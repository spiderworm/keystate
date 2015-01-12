keystate
========

Lightweight and expressive key handling for Javascript.

```js
if(keys.left) {
  console.log('left arrow key down');
}

if(keys.ctrl && keys.p) {
  paste();
}

if(keys.shift || keys[0]) {
  // do magic
}
```

## Installation

`npm install keystate`

or

`bower install keystate`


## Usage

Keystate gives you access to a keys object whose properties reflect the boolean states of the keys on your keyboard. Keystate uses `String.fromCharCode` (along with some predefined mappings) so that you can check the state of any alphanumeric key, along with the following list of modifiers.

Here's a list of predefined sequences that will map to key codes.

```
backspace
tab
enter
ctrl
alt
caps
esc
left
space
up
right
down
insert
delete
```

This library deliberately does not support event handling for keys. It's designed to be used in something with a run loop, that needs to check the state of the keys each time it runs.

If you need more advanced functionality, I suggest checking out [dmauro/Keypress](http://dmauro.github.io/Keypress/).
