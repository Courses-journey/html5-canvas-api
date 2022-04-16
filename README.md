# Canvas Api

Course Link

- [Learn Canvas API](https://www.youtube.com/playlist?list=PLDoPjvoNmBAxdetco1wwicE7Fbm73UYy0)

---

- Use cases:
  - Games
  - Photomanpulation
  - Audio and Video player
  - Charts
  - etc

---

# 02

- Important to know
  - [1] Canvas like img but without src + alt and with closing tag
  - [2] Canvas Can be styled wiht css
  - [3] Default value `width 300 \* height 150`
  - [4] Default value background-color is `transparent`

It's prefered to put width and height in canvas directly
`<canvas width="300" height="500"></canvas>`

u may face some stretch in content if width or height in css dosen't respect width and height ratio

if not width or height set to canvas in html or css `Default value is 300 * 150`

It's prefered to use id to get canvas as id is unique

---

# 03

Canvas have context this is where we draw our graphics we get it by `.getContext("id")` `id` to identify which type of graphics u want there are many like `2d` `webGl` and etc
usualy they name its var as `ctx` and name canvas var as `c`

Canvas Context method

- `.fillStyle =`

  - fill graphics with color | Gradient | pattern
  - Default value id `black`

- `.fillRect(x , y , width , height)`
  - draw rect

---

# 04

Canvas Context method

- `.createLinearGradient(x0 , y0 , x1 , y1)`

  - `x0` => Gradient Start from left
  - `y0` => Gradient Start from Top
  - `x1` => Gradient End to left
  - `y1` => Gradient End to Top
  - `.addColorStop(offset , color)`

- `.createPattern(image , "repeatation")`
  - `image` => image | video | another canvas
  - `repeatation` => `no-repeat` don't repeat pattern | `repeat` repeat pattern in all direction | `repeat-x` repeat pattern in x-axis | `repeat-y` repeat pattern in y-axis

Handle all these in a variable `var` the assign it to `.fillStyle = var`

---

# 05

Canvas Context method

- `.strokeStyle =`

  - fill graphics with color | Gradient | pattern
  - Default value id `black`

- `.fillstroke(x , y , width , height)`

  - draw rect border

- `.lineWidth =`

  - control line width

- `.setFont = "22px Tahoma"`

  - control font style

- `.fillText("some text")`

  - draw text

- `.strokeText("some text",x,y,maxwidth[opt])`
  - draw text border

---

# 05

Paths And Lines

Canvas Context method

- `.beginPath()`

  - to begin path drawing

- `.moveTo(x,y)`

  - to move brush to x and y u want
  - to begin path drawing

- `.lineTo(x,y)`

  - to draw points of line

- `.stroke()`
  - to show line

---

# 08

Paths Advanced Training

Canvas Context method

- `.closePath()`

  - to draw line from current postion to starting position

- `.fill()`
  - to fill closed path with certin color

---

# 09

Drawing Circle By Arc

Canvas Context method

- `.arc(x , y , raduis , startAngle , endAngle , antiClockwise [opt] = false`
  - `x & y` postion of centeriod
  - `raduis` raduis of circle
  - `startAngle` if set to `0` it will begin from 3 o'clock
  - `endAngle` radian value

```
Remember
360 Degree = Full Circle
1 Radian   = Half Circle => 1 pI => 3.14
2 Radian   = Full Circle => 2 pI => 6.28
```

---

# 10

Shadow Methods

Canvas Context method

- `.shadowColor = ""`

  - color of shadow
  - Accept all type of css like `hexColor` `rgba()` etc

- `.shadowBlur = 10`

  - Blurness of shadow
  - number value

- `.shadowOffsetX = "-20"`

  - move shadow in x direction
  - string value

- `.shadowOffsetY = "20"`
  - move shadow in y direction
  - string value

---

# 11

Transformation And Save, Restore Context

Canvas Context method

- `.scale(x,y)`

  - scale element in all `width | height | x postion | y postion`
  - `1` mean 100%

- `.save()`

  - save canvas context clean state
  - UseCase when need to `scale()` u put this before doing scale and u can use `resotre()` to back to normal

- `.restore()`

  - restore canvas context clean state

- `.translate(x,y)`
  - translate object by x and y and the origin is object transformation `(object.x,object.y)` not world origin `(0,0)`

---

# 12

Text Align And Direction

Canvas Context method

- `.textAlign = ""`

  - `start` => `left` | the main diffrence appear when change direction of canvas context the `left` will be the same but `start` will be changed
  - `end` => `right` | the main diffrence appear when change direction of canvas context the `right` will be the same but `end` will be changed
  - `center`

- `.direction = ""`

  - `rtl`
  - `ltr`

- `.globalAlpha = 1`
  - `1` mean 100% | `0.5` mean 50%
  - number value

---

# 13

It's recomended to draw your shape in single path

```
ctx.beginPath();

// Draw Here

ctx.fill();
```

or (Not recomended)

```
ctx.beginPath();

// Draw Here

ctx.moveTo(x,y) // x and y of next shape
```

---

# 14

End And Where To Continue

- [codepen](https://codepen.io/search/pens?q=canvas)
- [MDN Canvas Refrence](<[codePen.io](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas)>)
- [KIRUPA](https://www.kirupa.com/canvas/index.htm)
- [chartjs](https://www.chartjs.org/)
