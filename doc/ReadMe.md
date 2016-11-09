### 源码分析

* 路由用的vue-router，代码在 client/router中。
  其中menu.js存放的是侧边栏的配置。index中对menu。js进行处理。
  示例代码：

```js
  {
    name: 'Test', // 一级菜单名
    meta: {
      icon: 'fa-table', // 菜单icon，用的是font-awesome
      expanded: false   // 在sidebar弹出时，该子菜单是否展开
    },

    children: [ //二级菜单
      {
        name: 'TestChildren', // 在页面显示的菜单名
        path: '/tables/basic',  // 路由路径
        meta: {
          label: 'Test children'  // 有的话就是菜单栏显示的菜单名，如果没有，菜单栏显示的是name
        },
        component: lazyLoading('tables/Basic')  // 对应的页面（组件）
      }
    ]
```
