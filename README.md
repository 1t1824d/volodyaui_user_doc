## 开发指南

```
为了提升开发效率，实现绝大数功能开箱即用的目的，因此，对Echarts等插件进行二次封装。
```

## 安装

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


?> 通用点线面组合 Chart 图

```
   <component :is="'MyCustomPumpChartLine'" :itemChart="ChartData" :CustomConfig="{
          GraphicImg: require('./基础数据曲线背景1.png'),
          XFormatterConfig: Aciveitem.XFormatterConfig,
          YFormatterConfig: { IsFormatter: true, FormatterValue: 1 },
          GridConfig: {
            Left: 60,
            Right: 60,
            Top: 50,
            Bottom: 20
          },
          TooltipConfig: {
            XAxisName: '流量'
          },
          ScatterConfig: {
            SymbolSize: null,
            SymbolImg: ''//require('./星星.png')
          },
          PolygonDataConfig: {
            TextFillColor: '#333',
            MarkLineFontSize: 18,
            LineWidth: 0
          },
          PolylineDataConfig: {
            MarkPointDataConfig: {
              LabelColor: '#fff',
              LabelFontSize: 12,
              IsAllSymbol: false
            },
            TextFontSize: 16,
            SelectConfig: {
              FillColor: '#333',
              StrokeColor: '#D00907'
            }
          },
          DefaultLineConfig: {
            IsAllSymbol: false,
            SymbolIcon: 'circle',
            SymbolSize: 8,
            SymbolColor: 'yellow',
          },
          AxisLabelConfig: {
            FontSize: 12
          },
          LegendConfig: {
            FontSize: 12,
            FontColor: '#6E7B8B',
          },
          XAxisConfig: {
            FontSize: 12,
          },
          MarkLineConfig: {
            Padding: [-30, 0, -30, 46],
            SymbolSize: 10
          },
          IsGetDataURL: false
        }" @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun"
          @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun">
      </component>

```

!> itemChart 数据源

!> CustomConfig 自定义配置

```
       :CustomConfig="{
         GraphicImg: require('./基础数据曲线背景1.png'),//曲线背景图配置
          XFormatterConfig: {//x轴配置
             IsFormatter: true, //x轴标签是否格式化
             IsDate: true, //x轴标签是否显示日期
             FormatterValue: 'yyyy-MM-dd hh'
             //x轴标签传入的格式化条件
             （
             1.时间格式条件：'yyyy-MM-dd hh'，[详细参考Echarts文档](https://echarts.apache.org/zh/option.html#xAxis.axisLabel.formatter ':target=_blank')
             2.数值格式化条件：1或10或100  1---取整  10----保留一位小数  100保留两位小数 ...
             ）
              },
        YFormatterConfig: {//y轴配置
             IsFormatter: true, //y轴标签是否格式化
             FormatterValue: 1  //数值格式化条件：1或10或100  1---取整  10----保留一位小数  100保留两位小数 ...
             },
        GridConfig: {//Grid配置
          Left: 60,
          Right: 60,
          Top: 50,
          Bottom: 20
        },
        TooltipConfig: {//Tooltip配置
          XAxisName: '流量'
        },
         ScatterConfig: {//散点图自定义配置
            SymbolSize: null,
            SymbolImg: ''//require('./星星.png')
          },
        MarkLineConfig:{//标记线自定义配置
            Padding: [-30, 0, -30, 46],
            SymbolSize: 10
          }
          PolygonDataConfig: {
            TextFillColor: '#333',
            MarkLineFontSize: 18,
            LineWidth: 0
          },
          PolylineDataConfig: {
            MarkPointDataConfig: {
              LabelColor: '#fff',
              LabelFontSize: 12,
              IsAllSymbol: false
            },
            TextFontSize: 16,
            SelectConfig: {
              FillColor: '#333',
              StrokeColor: '#D00907'
            }
          },
          DefaultLineConfig: {
            IsAllSymbol: false,
            SymbolIcon: 'circle',
            SymbolSize: 8,
            SymbolColor: 'yellow',
          },
          AxisLabelConfig: {
            FontSize: 12
          },
          LegendConfig: {
            FontSize: 12,
            FontColor: '#6E7B8B',
          },
          XAxisConfig: {
            FontSize: 12,
          },

          IsGetDataURL: false//是否允许导出图片操作
        }"



    //在数据选中状态发生变化时触发的事件
    @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun">

    MyCustomChartSelectchangedFun(Data) {
      console.log(`MyCustomChartSelectchangedFun`, Data);
    }

    //点击导出图片
    @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun"

     MyCustomChartClickGetDataURLFun(DataURL, GetDataURLType) {
      console.log(`${GetDataURLType}DataURL`, DataURL);
    }
```


```
通用柱状图

<component :is="'MyCustomBarChart'" :itemChart="BarChartList"></component>

```

```
倒计时

  <my-clock textColor="red"></my-clock>//倒计时组件

```

```
按钮

  <my-button disabled>222</my-button>
  <my-button>333</my-button>

```
