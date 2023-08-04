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
                MarkLineConfig: {
                    Padding: [-30, 0, -30, 66],
                    SymbolSize: 30,
                    FontSize: 12
                },
                ScatterConfig: {
                    SymbolSize: null,
                    SymbolImg: ''//require('./星星.png')
                },
                PolygonDataConfig: {
                    TextFillColor: '#333',
                    MarkLineFontSize: 16,
                    MarkLineWidth: 3
                },
                PolylineDataConfig: {
                    MarkPointDataConfig: {
                        LabelColor: '#333',
                        LabelFontSize: 12,
                        SymbolIcon: 'arrow',
                        SymbolSize: 28,
                        SymbolColor: 'red',
                        SymbolBorderColor: '#222',
                        SymbolBorderWidth: 2,
                        SymbolBorderType: 'dashed',
                        IsLabel: false,
                        IsAllSymbol: false
                    },
                    TextFontSize: 16,
                    SelectConfig: {
                        FillColor: '#333',
                        StrokeColor: '#D00907'
                    }
                },
                DefaultLineConfig: {
                    MarkPointDataConfig: {
                        LabelColor: '#333',
                        LabelFontSize: 12,
                        SymbolIcon: 'arrow',
                        SymbolSize: 5,
                        SymbolColor: 'red',
                        SymbolBorderColor: '#222',
                        SymbolBorderWidth: 0,
                        SymbolBorderType: 'dashed',
                        IsLabel: false,
                        IsAllSymbol: true
                    },
                },
                YAxisConfig: ChartConfig.YAxisConfig,
                YFormatterConfig: [
                    { IsFormatter: true, FormatterValue: 10, Interval: 'auto' },
                    { IsFormatter: true, FormatterValue: 10, Interval: 'auto' }
                ],
                XAxisConfig: ChartConfig.XAxisConfig,
                XFormatterConfig: { IsFormatter: true, IsDate: true, FormatterValue: 'h', Interval: 240 },
                GridConfig: {
                    BackGroundColor: '#FFF',
                    BorderColor: '#222',
                    BorderWidth: 2,
                    GridIsShow: true
                },
                GridFormatterConfig: {
                    // Left: 60,
                    // Right: 60,
                    // Top: 50,
                    // Bottom: 20
                },
                TooltipConfig: {
                    XAxisName: '流量'
                },
                LegendConfig: {
                    FontSize: 12,
                    FontColor: '#6E7B8B',
                },
                GraphicImg: require('./chart/img/编组 24.png'),
                IsGetDataURL: false
            }" @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun"
                @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun">
      </component>

```

```
ChartConfig: {
                YAxisConfig: [
                    {
                        AxisLabel: {
                            Color: 'red',
                            IsShow: true,
                            FontSize: 12,
                            ShowMinLabel: null,
                            ShowMaxLabel: null
                        },
                        AxisLine: {
                            show: true,
                            symbol: [
                                'none',
                                'none'
                            ],
                            'symbolSize': [
                                10,
                                15
                            ],
                            'symbolOffset': [
                                0,
                                0
                            ],
                            'lineStyle': {
                                'color': 'red',
                                'width': 1,
                                'type': 'solid',
                                'dashOffset': 0,
                                'opacity': 1
                            }
                        },
                        AxisTick: {
                            'inside': false,
                            'length': 5,
                            'lineStyle': {
                                'color': '#222',
                                'dashOffset': 0,
                                'opacity': 1,
                                'type': 'solid',
                                'width': 1
                            },
                            'show': true
                        },
                        MinorSplitLine: {
                            lineStyle: null,
                            show: false
                        },
                        SplitArea: {
                            areaStyle: null,
                            interval: null,
                            show: false
                        },
                        SplitLine: {
                            linestyle: null,
                            show: false
                        },
                        show: true,
                        Name: '',
                        MinMax: null
                    },
                    {
                        AxisLabel: {
                            Color: 'red',
                            IsShow: true
                        },
                        AxisLine: {
                            lineStyle: null,
                            show: false,
                            symbol: null,
                            symbolOffset: null,
                            symbolSize: null
                        },
                        AxisTick: {
                            'inside': false,
                            'length': 5,
                            'lineStyle': {
                                'color': 'red',
                                'dashOffset': 0,
                                'opacity': 1,
                                'type': 'solid',
                                'width': 1
                            },
                            'show': true
                        },
                        'MinorSplitLine': {
                            'lineStyle': null,
                            'show': false
                        },
                        'SplitArea': {
                            'areaStyle': null,
                            'interval': null,
                            'show': false
                        },
                        'SplitLine': {
                            'linestyle': null,
                            'show': false
                        },
                        'show': true,
                        'Name': '',
                        'MinMax': null
                    }
                ],
                XAxisConfig: {
                    AxisLabel: {
                        Color: 'red',
                        IsShow: true,
                        FontSize: 12,
                        ShowMinLabel: null,
                        ShowMaxLabel: null
                    },
                    AxisLine: {
                        show: true,
                        symbol: [
                            'none',
                            'none'
                        ],
                        'symbolSize': [
                            10,
                            15
                        ],
                        'symbolOffset': [
                            0,
                            0
                        ],
                        'lineStyle': {
                            'color': 'red',
                            'width': 1,
                            'type': 'solid',
                            'dashOffset': 0,
                            'opacity': 1
                        }
                    },
                    AxisTick: {
                        'inside': false,
                        'length': 5,
                        'lineStyle': {
                            'color': '#222',
                            'dashOffset': 0,
                            'opacity': 1,
                            'type': 'solid',
                            'width': 1
                        },
                        'show': true
                    },
                    MinorSplitLine: {
                        lineStyle: null,
                        show: false
                    },
                    SplitArea: {
                        areaStyle: null,
                        interval: null,
                        show: false
                    },
                    SplitLine: {
                        linestyle: null,
                        show: false
                    },
                    show: true,
                    Name: '',
                    MinMax: null
                }
            },
```

!> itemChart 数据源

!> CustomConfig 自定义配置

```
      CustomConfig//自定义配置：{
                GraphicImg: require('./chart/img/编组 24.png')//背景图片。GraphicImg不配置或者为空时chart背景图片不加载,
                XFormatterConfig: { IsFormatter: true, IsDate: true, FormatterValue: 'h',Interval: 240 }//x轴格式化配置 IsFormatter 是否需要格式化 IsDate 是否是时间 FormatterValue 格式化的条件 如果是时间值为时间格式模板 h或hh 时,mm 分  具体参考：https://echarts.apache.org/zh/option.html#xAxis.axisLabel.formatter
                如果是数字传入数字1,10,100...分别表示取整、保留一位小数、保留二位小数....,Interval 标签间隔 "auto" 自适应 （具体参照Echars官方文档 https://echarts.apache.org/zh/option.html#series-custom.renderItem.return_polygon.x）
                 ....
            }



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
:CustomConfig="{
                MarkLineConfig: {
                    Padding: [-30, 0, -30, 66],
                    SymbolSize: 30,
                    FontSize: 12
                },
                ScatterConfig: {
                    SymbolSize: null,
                    SymbolImg: ''//require('./星星.png')
                },
                PolygonDataConfig: {
                    TextFillColor: '#333',
                    MarkLineFontSize: 16,
                    MarkLineWidth: 3
                },
                PolylineDataConfig: {
                    MarkPointDataConfig: {
                        LabelColor: '#333',
                        LabelFontSize: 12,
                        SymbolIcon: 'arrow',
                        SymbolSize: 28,
                        SymbolColor: 'red',
                        SymbolBorderColor: '#222',
                        SymbolBorderWidth: 2,
                        SymbolBorderType: 'dashed',
                        IsLabel: false,
                        IsAllSymbol: false
                    },
                    TextFontSize: 16,
                    SelectConfig: {
                        FillColor: '#333',
                        StrokeColor: '#D00907'
                    }
                },
                DefaultLineConfig: {
                    MarkPointDataConfig: {
                        LabelColor: '#333',
                        LabelFontSize: 12,
                        SymbolIcon: 'arrow',
                        SymbolSize: 5,
                        SymbolColor: 'red',
                        SymbolBorderColor: '#222',
                        SymbolBorderWidth: 0,
                        SymbolBorderType: 'dashed',
                        IsLabel: false,
                        IsAllSymbol: true
                    },
                },
                YAxisConfig: ChartConfig.YAxisConfig,
                YFormatterConfig: [
                    { IsFormatter: true, FormatterValue: 10, Interval: 'auto' },
                    { IsFormatter: true, FormatterValue: 10, Interval: 'auto' }
                ],
                XAxisConfig: ChartConfig.XAxisConfig,
                XFormatterConfig: { IsFormatter: true, IsDate: true, FormatterValue: 'h', Interval: 240 },
                GridConfig: {
                    BackGroundColor: '#FFF',
                    BorderColor: '#222',
                    BorderWidth: 2,
                    GridIsShow: true
                },
                GridFormatterConfig: {
                    // Left: 60,
                    // Right: 60,
                    // Top: 50,
                    // Bottom: 20
                },
                TooltipConfig: {
                    XAxisName: '流量'
                },
                LegendConfig: {
                    FontSize: 12,
                    FontColor: '#6E7B8B',
                },
                GraphicImg: require('./chart/img/编组 24.png'),
                IsGetDataURL: false
            }" @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun"
                @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun"
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
