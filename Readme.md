*This repository is a mirror of the [component](http://component.io) module [yields/shortcuts](http://github.com/yields/shortcuts). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-shortcuts`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# shortcuts

  keyboard shortcuts, similiar to [component/events](https://github.com/component/events).

## Installation

    $ component install yields/shortcuts

## Example

```js

function Editable(el){
  this.shortcuts = shortcuts(el, this);
  this.shortcuts.bind('command + z', 'undo');
  this.shortcuts.bind('command + b', 'bold');
}

Editable.prototype.undo = function(e){};
Editable.prototype.bold = function(e){};

```

## API

#### Shortcuts

  Bind shortcuts on the given `el` with `obj`.

### .k

  [k](/yields/k) instance

### #bind

  Bind `keys` with `method`

### #unbind

  Unbind all events, or `keys` or `keys` with `method`.

```js
shortcuts.unbind('command + z', 'undo') // => unbind `undo`, `command + z`
shortcuts.unbind('command + z'); // => unbind `command + z`
shortcuts.unbind(); // => unbind all
```

## License

  MIT
