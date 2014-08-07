Install
---

    $ component install kelonye/component-animate-cubic-bezier-curve

Usage
---

```javascript

  var canvas = document.createElement('canvas');
  canvas.width = 300.5;
  canvas.height = 300.5;
  document.body.appendChild(canvas);

  var ctx = canvas.getContext('2d');
  ctx.strokeStyle = '#aaa';
  ctx.moveTo(20.5, 20.5);
  ctx.bezierCurveTo(40.5, 100.5 , 200.5, 200.5, 220.5, 20.5);
  ctx.stroke();

  var animation = require('component-animate-cubic-bezier-curve');
  animation(20.5, 20.5, 40.5, 100.5 , 200.5, 200.5, 220.5, 20.5)
    .color('deepskyblue')
    .draw(canvas);

```

So,

```javascript

  var canvas = document.createElement('canvas');
  canvas.width = 300.5;
  canvas.height = 300.5;
  document.body.appendChild(canvas);

  var ctx = canvas.getContext('2d');
  ctx.strokeStyle = '#aaa';
  ctx.moveTo(20.5, 20.5);
  ctx.bezierCurveTo(40.5, 100.5 , 200.5, 200.5, 220.5, 20.5);
  ctx.stroke();

```

yields ...

![](https://dl.dropbox.com/u/30162278/component-animate-cubic-bezier-curve-a.png)

then,

```javascript

  var animation = require('component-animate-cubic-bezier-curve');
  animation(20.5, 20.5, 40.5, 100.5 , 200.5, 200.5, 220.5, 20.5)
    .color('deepskyblue')
    .draw(canvas);

```

yields ...

![](https://dl.dropbox.com/u/30162278/component-animate-cubic-bezier-curve-b.png)


Example
---

See [demo](http://component.herokuapp.com/#/53e3c7ea7d65b41900215c33)

    $ make example

## Api

### animation(ax, ay, bx, by, cx, cy, dx, dy)

  Initialize a new Animation with `ax`, `ay`, `bx`, `by`, `cx`, `cy`, `dx` and `dy` as

  ```javascript
  ctx.moveTo(ax, ay);
  ctx.bezierCurveTo(bx, by, cx, cy, dx, dy);
  ```

### Animation#color(string)

  Set the stroke style, which the animation will use

### Animation#draw(canvas)

  Initialize animation using `canvas` properties

License
---

MIT