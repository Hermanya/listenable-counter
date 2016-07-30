Counter example for [listenable browser](https://github.com/hermanya/listenable-browser)
----------------------------------------------------------------------------------------

This repo is basically a clone of [redux counter example](https://github.com/reactjs/redux/tree/master/examples/counter). The only modification I made is I added following code in ./components/Counter.js's `render` method:
```javascript
say(`Counter value is ${value}`).then(() => listenForUserInput({
    'increment': onIncrement,
    'increment if odd': this.incrementIfOdd,
    'increment asynchronously': this.incrementAsync,
    'decrement': onDecrement
}))
```

I also added a [polyfill](https://hermanya.github.io/listenable-browser/support_for_other_browsers.js) for other than listenable browsers:

```html
<script src="https://hermanya.github.io/listenable-browser/support_for_other_browsers.js"></script>
```
