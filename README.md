#html + css3实现太阳系模型

> [效果展示](https://wmlss.github.io/sunSystem/) 由于网络问题，可能加载较慢

#### 1. 各个星球轨迹的实现
  1. 先把边框变成一个圆然后利用css3的transform: rotateX(65deg);让圆形绕x轴3D旋转一定角度
  2. 然后把最外的包裹层的div利用transform: rotateZ(-8deg);这样就实现了平常我们认为的平面的星球轨迹的样子
#### 2. 各个星球的自转
  + css动画
  ```
  animation: circle 30s linear infinite;
  @keyframes circle {
    to {
      transform: rotate(1turn);
    }
  }
  ```
#### 3. 星球绕太阳公转（椭圆运动）
  1. 让星球先用transform-origin设置旋转的中心点然后旋转（圆运动）
  2. 然后星球的包裹层横向运动实现椭圆运动
