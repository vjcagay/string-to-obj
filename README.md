# String-to-Obj

> String to object properties parser for javascript

This module takes a string of key-value/value and transforms it to an object.

### Depends:

⇢ lodash >= 4.17.4


**Example:**

```js
const strToObject = require('str-to-obj');

config = {
    trim: true,
    delimiters: {
        values: {
            default: ','
        },
        keyValue: ':'
    },
    blackhole: 'context'
};

const parser = new strToObject(config);
console.log(parser.parse('tags:"db backup,systems" is:open is:active authors:johndoe,janedoe application crashes'));

/* Outputs:
[object Object] { 
  tags: ['db backup', 'systems'],
  is: ['open', 'active'],
  authors: ['johndoe', 'janedoe'],
  context: ['application', 'crashes']
}
*/
```

*No npm package yet! This project is still in progress of creating tests.*