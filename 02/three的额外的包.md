# three额外的包

1. **控制器**包:

   可以通过上下左右按键键或者鼠标拖拽, 移动相机, 控制显示位置

   这个包在源码的 `examples/js/controls/OrbitControls.js`位置,

   导入之后通过new 执行

```html
<script>
  // camera: 相机对象
  // renderer.domElement canvas dom对象
  import * as THREE from './path/to/three.module.js';
  import {OrbitControls } from './path/to/OrbitControls.js';
  // ...
  const controls = new OrbitControls(camera, renderer.domElement)
  controls.update()
  
  function animate(){
    requestAnimationFrame(animate)
    
    controls.update()
    // ...其余动画操作, 保持一致
    // 绘制
    renderer.render( scene, camera );
  }
</script>
```



