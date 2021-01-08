> wxml
```
<canvas class="canvas1" type="2d" canvas-id="c1"></canvas>
```
> wxss
```
  .canvas1{
  height: 500px;
  width: 300px;
  background-color: #f1f1f1;
}
```
> wxjs
```
  onLoad() {
    wx.createSelectorQuery().select(".canvas1").node(res=>{
      console.log(res)
      var canvas = res.node
      var x = canvas.getContext('2d')
      x.fillStyle = "red"
      x.fillRect(10,10, 150, 75)
    }).exec()
    // var context = wx.createCanvasContext('c1')
    // context.setFillStyle('red')
    // context.fillRect(10,10,150,75)
  },
  ```
