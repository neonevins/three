# three额外的包

1. 控制器包:

   可以通过上下左右按键键和鼠标拖拽, 移动相机, 控制显示位置

   这个包在源码的 `examples/js/controls/OrbitControls.js`位置,

   打包之后THREE.OrbitControls 存在

```html
<script src="./OrbitControls.js"></script>

<script>
	// camera: 相机对象
  // renderer.domElement canvas dom对象
  
  const controls = THREE.OrbitControls(camera, renderer.domElement)
  
</script>
```

