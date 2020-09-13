# #Fairy.css

Grid Flex toolkit

GitHub : [mafumafuultu/fairy.css](https://github.com/mafumafuultu/fairy.css)  
Demo : [fairly.css](https://mafumafuultu.github.io/fairy.css)

## Get started

```html
<link rel="stylesheet" href="./fairy.css">
```

## Compile less

Release

```sh
lessc ./pack.main.less fairy.css -x
```

Debug

```sh
lessc ./pack.main.less fairy.debug.css
```

## index
* Heading
* Grid
	* gap
* Flex
* Box
	* margin
	* padding
	* width
* Border
	* border radius
	* background grid
* Color
	* Background
	* Color
	* Theme
* Debug

## Heading

### `.f[level], .h[level], h[level]`
 
|[level]|font-size|
|-|-|
|1|3rem|
|2|2.25rem|
|3|1.5rem|
|4|1.25rem|
|5|1rem|
|6|0.875rem|

```html
<div class="h1">.h1 sample text</div>
<div class="h2">.h2 sample text</div>
<div class="h3">.h3 sample text</div>
<div class="h4">.h4 sample text</div>
<div class="h5">.h5 sample text</div>
<div class="h6">.h6 sample text</div>
```

## Grid
* Grid axis 1 - 13
* Grid trac 1 - 12
* [number] : 1 - 12

### `.grid`

```html
<div class="grid"></div>
```
```css
.grid { display: grid }
```

### `.g-[number]`
`grid-column-start: [number]`
### `.g-s-[number]`
`grid-column-start: span [number]`
### `.g--[number]`
`grid-column-end: [number]`
### `.g-s--[number]`
`grid-column-end: span [number]`

### `.g-r[number]`
`grid-row-start: [number]`
### `.g-s-r[number]`
`grid-row-start: span [number]`
### `.g--r[number]`
`grid-row-end: [number]`
### `.g-s--r[number]`
`grid-row-end: span [number]`

```html
<div class="grid">
	<div class="g-1"></div>
	<div class="g-s-1"></div>
	<div class="g--1"></div>
	<div class="g-s--1"></div>

	<div class="g-r1"></div>
	<div class="g-s-r1"></div>
	<div class="g--r1"></div>
	<div class="g-s--r1"></div>
</div>
```

### gap

#### `.gap-[level]`
 `grid-gap`

|[level]|`grid-gap`|
|-|-|
|1|3rem|
|2|2.25rem|
|3|1.5rem|
|4|1.25rem|
|5|1rem|
|6|0.875rem|


```html
<div class="grid gap-3">
	<div class="g-s-1"></div>
	<div class="g-s-1"></div>
	<div class="g-s-1"></div>
	<div class="g-s-1"></div>
</div>
```

## Flex

### `.flex`

```html
<div class="flex"></div>
```
```css
.flex { display: flex }
```

### `.f-g-[grow]`
`flex-grow: [grow]`

### `.f-s-[shrink]`
`flex-shrink: [shrink]`

### `.f-g-[grow_from]-[grow_to]`

```css
.f-g-1-4 {flex-grow: 1}
.f-g-1-4:hover {flex-grow: 4}
```

### `.f-ani.f-g-[grow_from]-[grow_to]`

```css
.f-ani {transition: flex-grow 200ms ease-in-out 100ms ;}
```

|number|range|
|-|-|
|[grow]|1 ~ 12|
|[shrink]|1 ~ 6|
|[grow_from]|1 ~ 6|
|[grow_to]|1 ~ 6|


## Box

### margin

|[number]|size|
|-|-|
|1|0|
|2|.125rem|
|3|.25rem|
|4|.5rem|
|5|1rem|
|6|2rem|

#### `.mar-[angle]-[number]`
[number]: 1 ~ 6

|[angle]|top|right|bottom|left|class|
|-|-|-|-|-|-|
|a |o|o|o|o|`.mar-a-[number]`|
|t |o| | | |`.mar-t-[number]`|
|r | |o| | |`.mar-r-[number]`|
|b | | |o| |`.mar-b-[number]`|
|l | | | |o|`.mar-l-[number]`|
|tb|o| |o| |`.mar-tb-[number]`|
|lr| |o| |o|`.mar-lr-[number]`|
|a-|o|o|o|o|`.mar-a--[number]`|

```html
<div class="mar-a-1"></div>
```

#### `.mar-a--[number]`

```html
<div class="mar-a--1">
	<div>target</div>
</div>
```

### padding
* [number]: 1 ~ 6

|[angle]|top|right|bottom|left|class|
|-|-|-|-|-|-|
|a |o|o|o|o|`.pad-a-[number]`|
|t |o| | | |`.pad-t-[number]`|
|r | |o| | |`.pad-r-[number]`|
|b | | |o| |`.pad-b-[number]`|
|l | | | |o|`.pad-l-[number]`|
|tb|o| |o| |`.pad-tb-[number]`|
|lr| |o| |o|`.pad-lr-[number]`|
|a-|o|o|o|o|`.pad-a--[number]`|

```html
<div class="pad-a-1"></div>
```

#### `.pad-a--[number]`

```html
<div class="pad-a--1">
	<div>target</div>
</div>
```

### width

#### `.w-[number]`
* [number]: from 0 to 100 step 10
* unit: %

```html
<div class="w-100"></div>
```


## Border

### target angle

|default style|top|right|bottom|left|class|
|-|-|-|-|-|-|
|none|||||`.bn` |
|solid |o|o|o|o|`.ba` |
|solid |o||||`.bt` |
|solid ||o|||`.br` |
|solid |||o||`.bb` |
|solid ||||o|`.bl` |
|solid||o|o|o|`.b-t`|
|solid|o||o|o|`.b-r`|
|solid|o|o||o|`.b-b`|
|solid|o|o|o||`.b-l`|

```html
<div class="bn"></div>
<div class="ba"></div>
<div class="bt"></div>
<div class="br"></div>
<div class="bb"></div>
<div class="bl"></div>
```

### `.b--[none, solid, dotted, dashed]`

`border-style`

```html
<div class="b--none"></div>
<div class="b--solid"></div>
<div class="b--dotted"></div>
<div class="b--dashed"></div>
```

### `.bw[number]`
`border-width`

|[number]|border-width|
|-|-|
|1|0|
|2|.125rem|
|3|.25rem|
|4|.5rem|
|5|1rem|
|6|2rem|

## border radius
### `.b-rad-[number]`
|[number]|border-radius|
|-|-|
|1|1px|
|2|2px|
|3|4px|
|4|.5rem|
|5|1rem|

## background grid

Display a grid of ruled lines on the background

### `.bg-g-s[number]`
|[number]|span|
|-|-|
|1|10px|
|2|15px|
|3|20px|
|4|25px|
|5|30px|

## Color
Specifying a color based on HSL

|hsl|default value|
|-|-|
|[hue]|from=0, to=360, step=10|
|[saturation]|100%|
|[lightness]|50%|

## Background

### `.bg-[hue]`

```html
<div class="bg-0"></div>
<div class="bg-10"></div>
<div class="bg-20"></div>
```

## Color

text color

### `.color-[hue]`

```html
<div class="color-0">text</div>
<div class="color-10">text</div>
<div class="color-20">text</div>
```
### `.color-c-[hue]`
Set the color of the text to be easier to read on a specified background color.

```html
<div class="darkness bg-0 color-c-0">text color white</div>
<div class="aurora bg-0 color-c-0">text color black</div>
```

## Theme

|class|[lightness]|
|-|-|
|`.darkness`|10%|
|`.dark`|30%|
|`.light`|70%|
|`.aurora`|90%|

|class|[saturation]|
|-|-|
|`.gray`|0%|

```html
<div class="darkness bg-0">darkness</div>
<div class="dark bg-10">dark</div>
<div class="bg-20">standard</div>
<div class="light bg-30">light</div>
<div class="aurora bg-40">aurora</div>
<div class="gray bg-50">aurora</div>
```

## Debug

### `.debug`
```css
.debug > * {border: solid .5px #000;}
```
