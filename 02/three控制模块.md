# threeJS控制模块

1. **控制器**包:

   可以通过上下左右按键键或者鼠标拖拽, 移动相机, 控制显示位置

   这个包在源码的 `examples/js/controls/OrbitControls.js`位置,

   导入之后通过new 执行
*   拖拽控制
```js

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

```

*   wsad控制
```js
import * as THREE from '../path/to/three.module.js'
const clock = new THREE.Clock()
import {FlyControls } from "../path/to/FlyControls.js"
function createControls(camera){
  const controls = new FlyControls( camera )
  controls.movementSpeed = 100;
  controls.rollSpeed = Math.PI / 6;
  controls.autoForward = false;
  controls.dragToLook = true;
  return controls
}
const controls = createControls(camera)
function animate(){
  requestAnimationFrame(animate)
  const delta = clock.getDelta();
  controls.update(delta)
  renderer.render( scene, camera );
}
animate()

```



