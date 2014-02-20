*This repository is a mirror of the [component](http://component.io) module [component/relative-date](http://github.com/component/relative-date). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-relative-date`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# relative-date

  Relative dates in words

## Installation

    $ component install component/relative-date

## Example

```js
var date = new Date(Date.now() - 60000);
console.log(relative(date) + ' ago');
// => "one minute ago"

var date = new Date(Date.now() + 5 * 60000);
console.log(relative(date) + ' from now');
// => "5 minutes from now"
```

## API

### relative(date)

  Return the `date` in words relative to `Date.now()`:

```js
var relative = require('relative-date');
var date = new Date(Date.now() + 2000);

var str = relative(date) + ' ago';
// => "2 seconds ago"
```

  An empty string `""` is returned when the difference
  is below one second. You may use this to default
  the string as shown here:

```js
var str = relative(new Date) || 'just now';
// => "just now"

var str = relative(new Date);
if (str) str = 'assignment due in ' + str;
else str = 'assignment due';
// => "assignment due"
```

### relative(date, other)

  Same as above, relative to `other` instead of `Date.now()`.

# License

  MIT
