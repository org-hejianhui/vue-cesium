# VUE CESIUM

<p align="center">
  <img src="https://zouyaoji.top/vue-cesium/favicon.png" width="200px">
</p>
<p align="center">基于 Vue 2.x 的Cesium三维地图组件。</p>

[![npm](https://img.shields.io/npm/v/vue-cesium.svg)]()
[![Travis](https://img.shields.io/travis/zouyaoji/vue-cesium.svg)]()
[![Package Quality](http://npm.packagequality.com/shield/vue-cesium.png)](http://packagequality.com/#?package=vue-cesium)
[![npm](https://img.shields.io/npm/dm/vue-cesium.svg)]()
[![license](https://img.shields.io/github/license/zouyaoji/vue-cesium.svg)]()

## 语言

- [中文](https://github.com/zouyaoji/vue-cesium/blob/master/README.zh.md)
- [English](https://github.com/zouyaoji/vue-cesium/blob/master/README.md)

## 文档

- [在线文档](https://zouyaoji.top/vue-cesium)
- [更多例子](https://github.com/zouyaoji/vue-cesium-demo)

## 开始

此项目引入的是构建后的 Cesium 包，也就是 Cesium 源码打包后`Build`目录的库。之所以这样是因为引入`Build`后的库可以随心所欲的切换在线、本地源，官方原生库和基于 Cesium 构建的第三方库。

逐步完善中，有问题可提 Issue 或者直接联系我交流。<370681295@qq.com>

### 安装

```bash
npm i --save vue-cesium
```

### 初始化

- 不指定 Cesium 库地址：

```javascript
import Vue from 'vue'
import VueCesium from 'vue-cesium'
// Vue-Cesium默认加载`https://unpkg.com/cesium/Build/Cesium/Cesium.js`
Vue.use(VueCesium)
```

- 指定 Cesium 库地址：

```javascript
import Vue from 'vue'
import VueCesium from 'vue-cesium'

Vue.use(VueCesium, {
  // cesiumPath 是指引用的Cesium.js路径，如
  // 项目本地的Cesium Build包，vue项目需要将Cesium Build包放static目录：
  // cesiumPath: /static/Cesium/Cesium.js
  // 个人在线Cesium Build包：
  // cesiumPath: 'https://zouyaoji.top/vue-cesium/statics/Cesium/Cesium.js'
  // 个人在线SuperMap Cesium Build包（在官方基础上二次开发出来的）：
  // cesiumPath: 'https://zouyaoji.top/vue-cesium/statics/SuperMapCesium/Cesium.js'
  // 官方在线Cesium Build包，有CDN加速，推荐用这个：
  cesiumPath: 'https://unpkg.com/cesium/Build/Cesium/Cesium.js'
})
```

```html
<template>
  <div class="viewer">
    <cesium-viewer> </cesium-viewer>
  </div>
</template>

<style>
  .viewer {
    width: 100%;
    height: 400px;
  }
</style>
```

### 使用

```vue
<template>
  <div class="viewer">
    <cesium-viewer> </cesium-viewer>
  </div>
</template>

<style>
.viewer {
  width: 100%;
  height: 400px;
}
</style>
```

## TODOS

- ~~关键属性不需在 ready 后用 Cesium 实例化，可以直接写到 data 中，一方面方便开发，另外一方面 watch 对象没那么复杂了，性能好些~~
- 用 rollupjs 打包改善局部引入
- 完善文档
- 继续增加常用组件
- ...

## 贡献

[贡献指南](https://github.com/zouyaoji/vue-cesium/blob/master/CONTRIBUTING.md)

## 协议

[MIT 许可证](https://opensource.org/licenses/MIT)

版权所有 (c) 2018 至今, zouyaoji <370681295@qq.com>

## 参考

学习参考了[vue-baidu-map](https://github.com/Dafrok/vue-baidu-map)
