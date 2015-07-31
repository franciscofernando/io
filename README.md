## Install
```shell
npm install io
```

## io.write(text, color/options, background, style)

**text(String): ** It is the text that will be printed.

**color(String): ** It is the color name that will contain the text(Default white).

**options(Object): ** It is an object that contains text styles

* **color(String): ** It is the color name that will contain the text(Default white).
* **background(String): ** It is the background color name that will contain the text(Default black).
* **style(String): ** It is the style that will contain the text.

**background(String): ** It is the background color name that will contain the text(Default black).

**style(String): ** It is the style that will contain the text.

```js
var io = require('io');
io.write('This text is red', 'red');
io.write('This text is yellow, background white and italic', {
   color: 'yellow',
   background: 'white',
   style: 'italic'
});
//Or
io.write('This text is yellow, background white and italic', 'yellow', 'white', 'italic');
```

## io.read(questions, callback)

**questions(Object): ** 
	* **question(String): **
	* **default(String): **
	* **format(RegExp): **
	* **formatError(String): **
	* **after(Function): **

```js
var io = require('io');
var question = {
    question: 'Age: ',
    defult: '18',
    format: /^.+$/,
    formatError: 'The format is incorrect, age:',
    after: function(answer){
	    this.continue();
    }
};
```