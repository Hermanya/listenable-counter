Counter example for listenable browser
--------------------------------------

This repo is basically a clone of [redux counter example](https://github.com/reactjs/redux/tree/master/examples/counter). The only modification I made is I added following code in ./components/Counter.js's `render` method:
```javascript
say(`Counter value is ${value}`).then(() => listenForUserInput({
    'increment': onIncrement,
    'increment if odd': this.incrementIfOdd,
    'increment asynchronously': this.incrementAsync,
    'decrement': onDecrement
}))
```

To be used outside the listenable browser, both `say` and `listenForUserInput` need to be [polyfilled](https://hermanya.github.io/listenable-browser/support-for-other-browsers.js) like so:

```html
<script src="https://hermanya.github.io/listenable-browser/support-for-other-browsers.js"></script>
```
