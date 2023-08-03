## 使用配置

?> 通用点线面组合 Chart 图

```
   <component :is="'MyCustomPumpChartLine'" :itemChart="ChartData" :CustomConfig="{
                MarkLineConfig: {
                    Padding: [-30, 0, -30, 66],
                    SymbolSize: 10,
                    FontSize: 12
                },
                ScatterConfig: {
                    SymbolSize: null,
                    SymbolImg: require('./chart/img/星星.png')
                },
                PolygonDataConfig: {
                    TextFillColor: '#333',
                    MarkLineFontSize: 16,
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
                YAxisConfig: ChartConfig.YAxisConfig,
                YFormatterConfig: [
                    { IsFormatter: true, FormatterValue: 1, Interval: '' },
                    { IsFormatter: true, FormatterValue: 1, Interval: '' }
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
                    Left: 60,
                    Right: 60,
                    Top: 50,
                    Bottom: 20
                },
                TooltipConfig: {
                    XAxisName: '流量'
                },
                LegendConfig: {
                    FontSize: 12,
                    FontColor: '#6E7B8B',
                },
                GraphicImg: IsChartGraphicChecked ? require('./chart/img/编组 24.png') : '',
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
