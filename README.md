## Vue3 总结

#### 一、Vue3 介绍

发布时间：2020年9月18日，Vue.js 发布 3.0 版本，One Piece（海贼王）
#### 二、Vue3 新特性

1.Composition API（组合API）
- setup 配置
- ref 与 reactive
- watch 与 watchEffect
- provide 与 inject

2.新的内置组件
- Fragment
- Teleport
- Suspense

3.其他改变
- 新的生命周期钩子
- data 选项应始终被声明为一个函数
- 移除keyCode支持作为 v-on 的修饰符

#### 三、升级 Vue3 的理由

1.性能提升
（1）打包大小减少 41%
（2）初次渲染快 55%, 更新渲染快 133%
（3）内存减少 54%

2.更好的支持 TypeScript

3.Composition API，更好的组件封装

#### 四、升级 Vue3 注意事项

1.适合升级 Vue3 的场景
2.不适合升级 Vue3 的场景
3.Vue3 与 Vue2 开发不兼容的注意要点

#### 五、Vue3 原理 & 源码解析

1.响应式原理
