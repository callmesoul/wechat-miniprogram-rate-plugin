# wechat-miniprogram-rate-plugin
微信小程序可高定制评分组件🌟

没找到合适的就自己做一个了，可换icon使用svg
大小颜色都可以随便调，满足一切需求

### 下载
``` bash
git clone https://github.com/callmesoul/wechat-miniprogram-rate-plugin.git
```

### 使用
1. 安装
```bash
npm install --save wechat-miniprogram-rate-plugin
```
2. 构建npm
微信开发者工具 -》 工具 -》 构建npm
3. 在你的页面json中添加
``` javascript
{
  "usingComponents": {
    "rate": "wechat-miniprogram-rate-plugin"
  }
}
```
4. 在wxml中即可使用组件
``` html
<rate></rate>
```


### Props

```
// 分值 一个图标1分 半个0.5分
    value: {
      type: Number,
      value: 0,
      observer() {
        this.initData()
      }
    },
    // 总共多少个图标
    count: {
      type: Number,
      value: 5,
      observer() {
        this.initData()
      }
    },
    // 图标没选中颜色
    color: {
      type: String,
      value: '#999999',
      observer() {
        this.initData()
      }
    },
    // 图标已选中颜色
    activeColor: {
      type: String,
      value: '#FFD731',
      observer() {
        this.initData()
      }
    },
    // svg图标的xml代码
    svg: {
      type: String,
      value: '<?xml version="1.0" standalone="no"?><!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"><svg t="1611282220789" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2723" xmlns:xlink="http://www.w3.org/1999/xlink" width="200" height="200"><defs><style type="text/css"></style></defs><path d="M749.226667 896a42.666667 42.666667 0 0 1-19.626667-4.693333L512 777.386667l-217.6 113.92a42.666667 42.666667 0 0 1-61.866667-45.226667l42.666667-240.213333-175.786667-170.666667a42.666667 42.666667 0 0 1-10.666666-42.666667 42.666667 42.666667 0 0 1 34.56-29.013333l243.2-35.413333 107.093333-218.88a42.666667 42.666667 0 0 1 76.8 0l108.373333 218.453333 243.2 35.413333a42.666667 42.666667 0 0 1 34.56 29.013334 42.666667 42.666667 0 0 1-10.666666 42.666666l-175.786667 170.666667 42.666667 240.213333a42.666667 42.666667 0 0 1-17.066667 42.666667 42.666667 42.666667 0 0 1-26.453333 7.68z" p-id="2724"></path></svg>',
      observer() {
        this.initData()
      }
    },
    // 一半值是否可选
    isHalf: {
      type: Boolean,
      value: true,
      observer() {
        this.initData()
      }
    },
    // 是否可点击
    disabled: {
      type: Boolean,
      value: false
    },
    // 每个图标的间隔rpx 最后一个没有
    marginRight: {
      type: Number,
      value: 5
    },
    // 每个图标宽度rpx
    width: {
      type: Number,
      value: 16
    },
    // 每个图标高度rpx
    height: {
      type: Number,
      value: 16
    },
```

### events

| name     | description              | parameters     |
| :---------------- | :----------------------- | :------  |
| change            |  改变了星星                | 改变的数值    |

### 贡献
如果你有好的意见或建议，欢迎给我提issue!
