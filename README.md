# Chart.js Linear Date and Time Charts
Chart.js line chart example with gradients and animations.

## Image

<img src="https://raw.githubusercontent.com/atomjoy/chartjs/refs/heads/main/chart-js.png" width="100%">
<img src="https://raw.githubusercontent.com/atomjoy/chartjs/refs/heads/main/chart-js-1.png" width="100%">

## Patterns and Gradients

### Image pattern

```js
const img = new Image();
img.src = 'https://example.com/my_image.png';
img.onload = () => {
  const ctx = document.getElementById('canvas').getContext('2d');
  const fillPattern = ctx.createPattern(img, 'repeat');

  const chart = new Chart(ctx, {
    data: {
      labels: ['Item 1', 'Item 2', 'Item 3'],
      datasets: [{
        data: [10, 20, 30],
        backgroundColor: fillPattern
      }]
    }
  });
};
```

### Stripes pattern

```js
function createDiagonalPattern(color = 'green') {
    let shape = document.createElement('canvas')
    shape.width = 10
    shape.height = 10
    let c = shape.getContext('2d')
    c.strokeStyle = color
    c.beginPath()
    c.moveTo(2, 0)
    c.lineTo(10, 8)
    c.stroke()
    c.beginPath()
    c.moveTo(0, 8)
    c.lineTo(2, 10)
    c.stroke()
    return c.createPattern(shape, 'repeat')
}

const chart = new Chart(ctx, {
  type: 'bar',
  data: {
    labels: ['Item 1', 'Item 2', 'Item 3'],
    datasets: [{
      data: [10, 20, 30],
      backgroundColor: createDiagonalPattern('#09f'),
    }]
  }
});
```

## Links
- https://www.chartjs.org/docs/latest/
- https://www.chartjs.org/docs/latest/general/colors.html#patterns-and-gradients
- https://www.chartjs3.com/docs/chart/getting-started
- https://www.youtube.com/watch?v=DnjlLbOsPlM
- https://www.youtube.com/watch?v=AEaXyzCElGI
- https://www.youtube.com/watch?v=vmp3czGfw2U
- https://www.youtube.com/watch?v=EVHi41f7psQ
