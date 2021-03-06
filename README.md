# ngraph.expose

Adds getters and setters to subset of object's properties

 [![build status](https://github.com/anvaka/ngraph.expose/actions/workflows/tests.yaml/badge.svg)](https://github.com/anvaka/ngraph.expose/actions/workflows/tests.yaml)

# Example

``` js
var target = {};
var source = { age: 42};

exposeProperties(source, target);

target.age(); // returns 42
target.age(24); // sets source.age to 24;

```

You can also select only subset of properties you want to expose:

``` js
var target = {};
var source = { age: 42, name: 'John'};
exposeProperties(source, target, ['name']);
target.name(); // returns 'John'
target.age === undefined; // true
```

# install

With [npm](https://npmjs.org) do:

```
npm install ngraph.expose
```

# license

MIT
