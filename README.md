# Selective FastClick

A very early hack together of FT's [FastClick](http://github.com/ftlabs/fastclick) with [DOM Delegate](http://github.com/ftlabs/ftdomdelegate) libraries.

## Installation

```
npm install selective-fastclick
```

And `require` with Browserify. Or [download the prebuilt package](http://wzrd.in/standalone/selective-fastclick@latest)

## Demonstration

[See a simple demonstration of Selective FastClick](http://matthew-andrews.github.io/selective-fastclick/examples/demo.html)

## Usage
If using the prebuild package use:
```js
window.selectiveFastclick.attach(document.body, selectors);
```

```js
var SelectiveFastClick = require('selective-fastclick');

var selectors = [
  'button',
  '.elements-with-class',
  '#element-with-this-id',
  'div.delegate-test-clickable + #another-delegate-test-clickable'
];

SelectiveFastClick.attach(document.body, selectors);
```

Or, if you use the **prebuilt package**:-

```js
selectiveFastclick.attach(document.body, selectors);
```

The first argument of `attach` is the element to attach the event delegator to - and the second argument is a string or array of strings of selectors to match against to provide 'FastClick' behaviour.  Please see the documentation of FastClick for an explanation of what it does the documentation of FT DOM Delegate for details on which selectors are supported.

## Credits and collaboration ##

The lead developer of Selective FastClick is [Matt Andrews](http://twitter.com/andrewsmatt) at FT Labs. All open source code released by FT Labs is licenced under the MIT licence. We welcome comments, feedback and suggestions.  Please feel free to raise an issue or pull request.
