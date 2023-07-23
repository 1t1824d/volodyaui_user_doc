
## 开发指南

```
为了提升开发效率，实现绝大数功能开箱即用的目的，因此，对Echarts等插件进行二次封装。
```

##  安装

  

```

npm install volodyaui

```

## 引入



```

import volodyaui from "volodyaui"
import "volodyaui/volodyaui.css";
Vue.use(volodyaui)

```

## 使用


```
   <component :is="'MyCustomPumpChartLine'" :itemChart="ChartData" :CustomConfig="{
        GraphicImg: require('./基础数据曲线背景1.png'),
        XFormatterConfig: { IsFormatter: true, IsDate: true, FormatterValue: 'yyyy-MM-dd hh' },
        YFormatterConfig: { IsFormatter: true, FormatterValue: 1 },
        GridCofig: {
          Left: 60,
          Right: 60,
          Top: 50,
          Bottom: 20
        },
        TooltipConfig: {
          XAxisName: '流量'
        }
      }">
      </component>

```

```

  <my-clock textColor="red"></my-clock>//倒计时组件

```

```

  <my-button disabled>222</my-button>  //按钮
  <my-button>333</my-button>

```



