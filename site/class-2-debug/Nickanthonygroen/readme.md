# Scatter plot

A simple responsive scatter plot visualising the dimensions of sepals and petals
of various iris flowers based on a [`bl.ock`][block] by
[**@mbostock**][block-author] (GPL-3.0).

[![][cover]][url]






## Background

In this assignment we had to find bugs in the files and debug them. We also had to refactor the files from d3.v3 to d3.v4.


### Debug & Refactor

Change the D3 from v3 to v4.

```
<script src="https://d3js.org/d3.v4.min.js"></script>

```


From this


```js

var width = 960 - margin.l - margin.r;
var height = 500 - margin.t - margin.b;

```

to this

```js

var width = 960 - margin.left - margin.right;
var height = 500 - margin.top - margin.bottom;
```


```js
function onload(data) {
  x.domain(d3.extend(data, sepalWidth)).nice();
```


```js
function onload(data) {
  x.domain(d3.extend(data, sepalWidth)).nice();
```


A number of times there were functions weren't added to the variables so i hdit this several times.

```js
svg
  .append('g')
  .attr('class', 'x axis')
```

to
```js
svg.append('g')
  .attr('class', 'x axis')
```


## Features

*   [`d3.scale.linear`](https://github.com/d3/d3-3.x-api-reference/blob/master/Quantitative-Scales.md#_linear)
*   [`d3.scale.ordinal`](https://github.com/d3/d3-3.x-api-reference/blob/master/Ordinal-Scales.md#ordinal)
*   [`d3.svg.axis`](https://github.com/d3/d3-3.x-api-reference/blob/master/SVG-Axes.md#axis)
*   [`d3.extent`](https://github.com/d3/d3-3.x-api-reference/blob/master/Arrays.md#d3_extent)
*   [`d3.csv`](https://github.com/d3/d3-3.x-api-reference/blob/master/CSV.md#csv)

## License

GPL-3.0 © Titus Wormer

[block]: https://bl.ocks.org/mbostock/3887118

[block-author]: https://github.com/mbostock

[cover]: preview.png

[url]: https://cmda-fe3.github.io/course-17-18/class-2/debug