# vue-qqmap
<p align="center">
  <img src="https://static.only1314.cn/public/images/vqqmap-logo.png" width="200px">
</p>
<p align="center">基于Vue 3.x的腾讯地图插件</p>

#####  简称：vqqmap
> 基于Vue3的腾讯地图可视化拾取、描点，路径规划插件<br>
## 语言

- [中文](https://github.com/cuteCloud/vue-qqmap/blob/master/README.zh.md)
- [English](https://github.com/cuteCloud/vue-qqmap/blob/master/README.md)


![效果展示](https://static.only1314.cn/public/images/vqqmap01.jpg "效果展示")

[DEMO 演示](https://codesandbox.io/s/goofy-northcutt-y0sz7)

## 特征
1. TS编写，高效且轻量
2. 使用简便,轻量美观
2. 支持腾讯地图原生所有Options
3. 更多特性将在未来得到支持

<p>如果你有任何疑问、建议或发现了Bug , 最快的解决方式是请您提交issues!</p>
<p>如果你喜欢 , 请给一个小star, 十分感谢!</p>
<p>如果有需要，后续可以出一个vue2.x版本!</p>


## 安装方式
### With npm
``` bash
$ npm install vue-qqmap
```

## 使用:
``` html
<vqqmap v-model="location" @update="mapChange" :options="options"></vqqmap>
```
``` js
  ...
  import vqqmap from 'vue-qqmap'
  ...
  export default defineComponent({
      components: { vqqmap },
      setup() {
        let location = reactive({lat:'',lng:'',address:''})
        let options= reactive({
          key:'Yours Key',
        })
        function mapChange(data){
          console.log(data)
        }
        return {
          location,
          options,
          mapChange
        };
  },
});
  ...
```

## **v-model**
Type: `Object|Array`<br>
Required: `true`<br>
Default: `{lat:'',lng:'',address?:''}|[{lat:'',lng:'',address?:''},{lat:'',lng:'',address?:''}]`<br>

## **props**

您可以向组件传入以下prop

### multiple
Type: `Boolean`<br>
Required: `false`<br>
Default: `false`<br>
if you want to set multiple  marks，should open it

### options
除了以下的配置项，您还可以使用腾讯地图自带的所有配置项
###### key
Type: `String`<br>
Required: `true`<br>
[没有Key，去申请？](https://lbs.qq.com/)

###### width
Type: `String,Number`<br>
Required: `false`<br>
Default: `700`<br>

###### height
Type: `Number`<br>
Required: `false`<br>
Default: `400`<br>

###### showHeader
Type: `Boolean`<br>
Required: `false`<br>
Default: `true`<br>

###### showFooter
Type: `Boolean`<br>
Required: `false`<br>
Default: `true`<br>

###### showBorder
Type: `Boolean`<br>
Required: `false`<br>
Default: `true`<br>

###### zoom
Type: `Number`<br>
Required: `false`<br>
Default: `12.2`<br>

###### disabledClick
Type: `Boolean`<br>
Required: `false`<br>
Default: `false`<br>

当然，你可以使用腾讯地图原生的所有options，[ 查看更多！ ](https://lbs.qq.com/webApi/javascriptGL/glDoc/docIndexMap#2)

## **事件**
`update` 当坐标或者地址发生改变时触发

[blog](https://blog.only1314.cn/)
