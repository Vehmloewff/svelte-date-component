# svelte-date-component

A svelte component for displaying the amount of elapsed time since a given date.

## Usage
Add it to your svelte project:
```shell
$ npm i svelte-date-component --save
```
Then, pop it into the component that suites you:
```html
<script>
	import Elapsed from 'svelte-date-component';
	let date = new Date().getTime();
</script>

<Elapsed mils={date}/>
```
As you can see `svelte-date-component` has only one prop:  `mils` of type number.

The above example would display this:
```
Just now
```
... until 3 seconds has elapsed, then it would display:
```
4 seconds ago
```


This example...
```html
<script>
	import Elapsed from 'svelte-date-component';
	let date = new Date().getTime() - 1000 * 60 * 60 * 24; // One day before now
</script>

<Elapsed mils={date}/>
```
...displays this:
```
About a day ago
```

## Bugs
Found an problem? [Submit an issue](https://github.com/Vehmloewff/svelte-date-component/issues/new), or ping me on Discord: Vehmloewff#0724.