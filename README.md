# vue-qqmap

#### 简称：vqqmap

> 基于Vue3的腾讯地图地址可视化拾取、描点，路径规划插件<br>

[DEMO-todo···](https://blog.only1314.cn/)

![效果展示](https://static.only1314.cn/public/images/vmap-demo01.jpg "效果展示")

## Features
1. Simple and easy to use, light and beautiful
2. Support native map all configuration
3. More features will be provided in the future

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
In addition to the following configuration, you can also use all Tencent Map Options
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

##### zoom
Type: `Number`<br>
Required: `false`<br>
Default: `12.2`<br>

Of course，you can use other tencent map options，[ look more！ ](https://lbs.qq.com/webApi/javascriptGL/glDoc/docIndexMap#2)



## Events
`update` Triggered when coordinates and addresses change

