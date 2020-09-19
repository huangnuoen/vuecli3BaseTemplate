# vuecli3BaseTemplate
基于vuecli3搭建的移动端开发模板，框架vant+axios
## 介绍
适用于移动端快速开发
这个配置也用在了多个项目上，平时做项目就直接在这个基础上开发，不需要每次都在自己配一遍，基础功能满足日常移动端开发，方便快捷。有兴趣朋友可以瞧一瞧试一试，有什么问题欢迎提issues
```
npm install

npm run serve

npm run build
```

1. 适用于移动端快速开发，直接用px进行开发即可（基于蓝湖设计稿750px），默认用postcss转换成vw
2. ui框架 vant(按需引入)
3. 请求，引入了axios 并做了封装

vue+webpack4+vant+axios+less+postcss+prettier

## 文件目录

## 功能

### 全局样式变量

已全局引入less样式变量 
变量在 `src/style/variable.less`文件中定义，`.vue` 单文件和`.less` 都可以直接使用
```less
// `src/style/variable.less`
@theme: #ffab11; // 主题色
@theme2: #fa9716; // 次级主题色
// 使用
.text {
  color: @theme;
  background-color: @theme2;
}

```
### api 请求
异步请求使用axios, 这也是vue 官方推荐使用的框架。
#### 封装思路
1. `api/index.js` 中导出所有`api`
2. 在`api/config.js`对 axios 作了一层封装
3. 接口模块化管理，命名统一使用后台提供的接口路径，如套餐模块的接口在 api/package, 收藏接口在 api/collect
   1. 采用后台接口命名是为了和后台统一，有异议的可以不遵循，
4. `api/index.js` 中导出所有`api`,并且挂载在 vue.prototype.api 上，在` vue` 单文件中不需要再引入，可以直接调用`this.$api.collect.add()`
   
这里对它做了一层封装，最后挂载在Vue.prototype.$api上

#### 使用


#### 响应拦截
#### 写法规范
### vant 按需引入
### 全环境打包
### 一键打包上传
### svg icon
### 列表详情缓存
### 指令: 波纹按钮 input bug fixed
### 通用方法封装
#### 滚动穿透
#### 倒计时
#### 日期格式化
### 通用组件封装
#### 滚动顶部
#### 空状态
#### loading
#### titlebar
#### 过渡效果
### filter
#### 价格格式化
### 微信分享封装
### 登录授权封装
### vuex 持久化
### 适配iphonex 底部