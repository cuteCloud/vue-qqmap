# vue-qqmap

####简称：vqqmap

> 基于Vue3的腾讯地图地址可视化拾取、描点，路径规划插件<br>

[DEMO-todo···](https://blog.only1314.cn/)

![效果展示](https://static.only1314.cn/public/images/vqqmap-demo.jpg "效果展示")

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
#### All options
Tencent map native API will be fully supported in succession, but currently only support the following configuration
##### key
Type: `String`<br>
Required: `true`<br>
[No Key, go apply？](https://lbs.qq.com/)

##### width
Type: `String,Number`<br>
Required: `false`<br>
Default: `700`<br>

##### height
Type: `Number`<br>
Required: `false`<br>
Default: `400`<br>

## Features
1. Simple and easy to use, light and beautiful
2. The installation is provided as' NPM '
3. More features will be provided in the future


## Events
`update` Triggered when coordinates and addresses change

