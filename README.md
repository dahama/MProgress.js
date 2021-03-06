MProgress.js
============

Google Material Design Progress Linear bar.

It using CSS3 and pure js which don't depend on any other libraries.

## Types and preview

Type 1. `Determinate`

<img src="https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/determinate.gif" />

Type 2. `Buffer`

<img src="https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/buffer.gif" />

Type 3. `Indeterminate`

<img src="https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/indeterminate.gif" />

Type 4. `Query Indeterminate and  Determinate`

<img src="https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/query.gif" />


Or you can see all types together:

[Vedio：Material Progress & activity](http://material-design.storage.googleapis.com/publish/v_2/material_ext_publish/0B0NGgBg38lWWYmNmallST001a1k/components-progressactivity-typesofindicators-061101_Linear_Sheet_xhdpi_003.webm)

### DEMO

[See the Online demo](http://lightningtgc.github.io/MProgress.js/)

## How to start

#### Install it

Including [mprogress.js] and [mprogress.css] into your target html file.

```html
<link rel='stylesheet' href='mprogress.css'/>

<script src='mprogress.js'></script>
```

## Basic usage

Example for the `Determinate` type

1.Instantiation:

```js
var mprogress = new Mprogress();
```

2.Show and start the bar by using:

```js
mprogress.start();
```

Or you can just use `the following code` to replace step 1 and 2:

```js
var mprogress = new Mprogress('start');
```

3.Finish the loading and hide it :

```js
mprogress.end();
```

## Advanced usage

All types have `start` and `end` methods.

#### Type1:Determinate

`Determinate` also have `set` and `inc` methods.

##### set(n)

sets the progress bar status, where `n` is a number from `0.0` to `1.0`.

eg:
```js
mprogress.set(0.3);
```

##### inc()

increases by a random amount.

eg:
```js
mprogress.inc(); // Increase the bar with a random amount.
mprogress.inc(0.3); // This will get the current status value and adds 0.3 until status is 0.994
```


#### Type2:Buffer 

It always used for vedio loading,and you can using for other case.

Init Type Buffer :

```js
var bufferIntObj = {
  template: 2
};
var bufferProgress = new Mprogress(bufferIntObj);
```

##### Start it:

```js
bufferProgress.start();
```

If you want to start it immediately when instantiate it，you can use:

```js
var bufferIntObj = {
  template: 2, // type number
  start: true
};
var bufferProgress = new Mprogress(bufferIntObj);
```

##### End it: 

```js
bufferProgress.end();
```

`Buffer` also have `set` , `inc` and `setBuffer` methods

Type `Buffer` has two progress: main progress and buffer progress.

##### `set(n)` 

sets the main progress bar status (0,1)

##### `setBuffer(num)` 

sets the buffer progress bar status (0,1)

#### Type3:Indeterminate 

Init Type Indeterminate :

```js
var intObj = {
  template: 3, 
  parent: '#customId' // this option will insert bar HTML into this parent Element 
};
var indeterminateProgress = new Mprogress(intObj);
```

Type Indeterminate just has `start` and `end` methods.

```js
indeterminateProgress.start();
indeterminateProgress.end();
```

#### Type4:Query Indeterminate and Determinate 

Init Type Query :

```js
var intObj = {
  template: 4,
  parent: '#anothercustomId' // in other position
};
var queryProgress = new Mprogress(intObj);
```

Type Query just has `start` and `end` methods.

```js
queryProgress.start();
queryProgress.end();
```

## Configuration

Passing an object(configuration) to instantiated Mprogress

#### template

#### parent

#### start

##### minimum

##### easing

## Browser Support



## License

[MIT](http://opensource.org/licenses/mit-license.php)  © [gctang](https://github.com/lightningtgc)
