# vue-qqmap
<p align="center">
  <img src="http://static.cutetool.cn/vqqmap-logo.png" width="200px">
</p>
<p align="center">Tencent Map Plugin for Vue 3.x</p>

#####  Shorter Name：vqqmap
> Vue3 - based Tencent map visual pick up, tracing points, path planning plug-in<br>
## Languages

- [中文](https://github.com/cuteCloud/vue-qqmap/blob/master/README.zh.md)
- [English](https://github.com/cuteCloud/vue-qqmap/blob/master/README.md)


![Results show](http://static.cutetool.cn/vqqmap01.jpg "Results show")

## Features
1. Simple and easy to use, light and beautiful
2. Support native map all configuration
3. More features will be provided in the future

<p>If you like , please give me star,thanks!</p>
<p>If you have some question , please submit issues!</p>

## Installation
### With npm
``` bash
$ npm install vue-qqmap
```

## Typical use:
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

You can send these props to the component


### multiple
Type: `Boolean`<br>
Required: `false`<br>
Default: `false`<br>
if you want to set multiple  marks，should open it

### options
In addition to the following configuration, you can also use all Tencent Map Options
###### key
Type: `String`<br>
Required: `true`<br>
[No Key, go apply？](https://lbs.qq.com/)

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

Of course，you can use other tencent map options，[ look more！ ](https://lbs.qq.com/webApi/javascriptGL/glDoc/docIndexMap#2)

## **Events**
`update` Triggered when coordinates and addresses change

[blog](https://blog.only1314.cn/)

