# Upgrading

## From v3.x to v4.x
There is no change if you are consuming this package in module environment like webpack.
If you were consuming this package directly in browser environment then update your code -
```diff
- Vue.use(VueWebStorage)
+ Vue.use(VueWebStorage.default)
```

## From v2.x to v3.x
* The `driver` configuration property has been renamed to `drivers`.
* The `drivers` property now can accepts array of drivers, for example
```js
Vue.use(Storage, {
  drivers: ['local','session']
})
```
* The prefix property should work same as before.
```js
Vue.use(Storage, {
  prefix: 'your_app_',
})
```
* All API methods now available on `$localStorage` or `$sessionStorage` based on drivers specified in configs.
* In order to preserve old behaviour you have to rename all occurrences of `Vue.$storage` with appropriate name.
* All methods name, and their behaviour remains same.
