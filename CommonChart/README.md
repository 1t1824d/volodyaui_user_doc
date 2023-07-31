## 使用配置

?> 通用点线面组合 Chart 图

```
   <component :is="'MyCustomPumpChartLine'" :itemChart="ChartData" :CustomConfig="{
          GraphicImg: require('./基础数据曲线背景1.png'),
          XFormatterConfig:{ IsFormatter: true, IsDate: false, FormatterValue: 1 ,Interval:999},
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
             Interval：999，//标签间隔
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


## 数据源字段说明

<details>
<summary>数据源字段说明（点击展开）</summary>

[数据源字段说明](./Config.json ":include :type=code")

</details>

## 数据源示例

<details>
<summary>数据源字段说明（点击展开）</summary>

[数据源示例](./Data.json ":include :type=code")

</details>
