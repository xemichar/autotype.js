# autotyped.js
autotyped.js is a library that types any string.

[Demo](https://vuksamardzic.github.io/autotyped.js/)

### Includes

Just add a link to the css file in your `<head>`:

```html
<link rel="stylesheet" type="text/css" href="./lib/autotyped.css"/>
```

Then, before your closing ```<body>``` tag add:

```html
<script type="text/javascript" src="./lib/autotyped.min.js"></script>
```

### Usage
```html
<h1 class="at-init">Text to be autotyped!</h1>
```

```html
<script>
    const autotyped = new Autotyped();
    autotyped.init();
</script>
```

### Settings

Option | Type | Default | Description
------ | ---- | ------- | -----------
selector | string | '.at-init' | CSS selector.
animate | boolean | true | Choose whether you animate or not.
animation | string | 'bounce' | Choose which animation you use. Available `'bounce'`, `'rotate'`, `'rubber-band'`, `'pop-in'`, `'left-slide'`, `'right-slide'`, `'meteor-shower'`.
speed | int | 200 | Autotype speed in ms.
text | string[] | [] | Text you feed to autotyped.js

### Example
```html
<p class="at-init">Text to be autotyped!</p>
 
<script>
    //we want it to go faster or slower than default (200)
    const autotyped = new Autotyped();
    autotyped.init({speed: 100});
</script>
```
```html
<p class="at-init">Text to be autotyped!</p>
 
<script>
    //we somehow don't want animations... weird.. but hey, your choice
    const autotyped = new Autotyped();
    autotyped.init({animate: false});
</script>
```
```html
<p id="myElement">Text to be autotyped!</p>
 
<script>
    //we want specific selector with custom speed and other animation
    const autotyped = new Autotyped();
    autotyped.init({speed: 250, animation: 'rotate', selector: '#myElement'});
</script>
```
#### License

Licensed under the MIT license.

Made with :heart: by Vuk Samardžić.
