# iview 踩坑记录



官网首页 https://weapp.iviewui.com/



**Cannot read property 'handleShow' of null  错误**

在小程序 .json添加

```js
"navigationBarTitleText": "添加随访",

  "usingComponents": {

​    "i-toast": "../../../../iview/toast/index"

  }
```

在页面 .wxml 顶端或者底部添加

```html
<i-toast id="toast" />
```

在 .js文件引入  并使用

```js
const { $Toast } = require('路径/base/index');

$Toast({
    content: '随访计划名称不能为空'
});
```

