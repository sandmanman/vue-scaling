# vue-scaling
基于vue开箱即用缩放组件
(A super easy zomm components for Vue!)
# pc & wap 端效果
![双击缩放或者移动到原点](https://1img.evente.cn/84/23/24/91d3e0e8561ea75bf9e4adcfdf.jpg?imageView2/2/w/740)
![双击缩放或者移动到原点](https://0img.evente.cn/69/1e/19/bcfd8bc55db61d537324789c18.jpg?imageView2/2/w/740)

# 如果图片打不开...
[掘金地址](https://juejin.im/post/5df89e0c51882512243f9ca8) 

# 安装
```
npm i vue-scaling
```
# 使用组件
##### 注册
```
// 全局
import vueScaling from 'vue-scaling'
Vue.use(vueScaling)
```

##### 使用
```
// 组件需要设置宽高样式
<vueScaling style="width: 400px;height:400px;overflow: hidden" ref="vueScalingRef">
  <div style="background:rgba(97, 72, 72, 0.5);width:400px;height:400px"></div>
</vueScaling>
```

# 特性
- 使用 TypeScript 构建，完整的单元测试，提供完整的类型定义文件。
- 现代浏览器和 IE9 及以上。
- pc&wap 通用的缩放放大点击 Vue 组件 开箱即用。

# API
### 参数
属性 | 含义 |  类型 |默认值 | 是否必填
---|---|---|---|---
maxScale| 最大缩放倍数 | Number | 2 | 否|
minScale| 最小缩放倍数 | Number | 0.5 | 否|
tapNumber| 进行缩放的点击次数(可填 1 or 2) | Number | 2 | 否|
stopBorder| 如果stopBorder阻力大于0 移动时将会有边界判定 | Number | 0 | 否|
animation | 初始动画(在加载完成后会有一个动画效果) | Boolean | false | 否|

### emit方法
属性 | 含义 |  返回值 | 是否必填
---|---|---|---
moveChange| 移动时的emit | {point2DObj: {x, y}, tMatrix: matrix数组} |  否 |
scaleChange| 缩放时的emit | {scale, {x, y}, tMatrix: matrix数组} |  否 |

### 内置方法 通过this.$refs.vueScalingRef 调用
- this.$refs.vueScalingRef.backState() 回到初始状态

# 注意
通过改变css的overflow:hidden即可实现 拖动缩放隐藏边界的效果

### 相关参考
1. [vue-TypeScript](https://cn.vuejs.org/v2/guide/typescript.html) 
2. [vue-touch](https://github.com/vuejs/vue-touch)
3. [matrix](https://www.jianshu.com/p/956d54376338) 
...

### 如果你觉得这个项目有趣 务必请给个star~ (҂‾ ▵‾)σ(˚▽˚’!)/
[给我star~](https://github.com/whorcare/vue-scaling)

### 交流
##### 有什么意见,或者bug 或者想一起开发vue-scaling
![我的微信](https://0img.evente.cn/0f/41/65/8ad030fc5d9f82f6345b3d6e7c.jpg?imageView2/2/w/220)

### ISS
[提iss](https://github.com/whorcare/vue-scaling/issues/new)

### 更新日志
#### v0.2.0
- 删除 width,height 参数。推荐改写为css样式作用在组件上
- 增加初始化加载动画
