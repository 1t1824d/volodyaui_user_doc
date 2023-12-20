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
<div class="ChartBox">
         <component
          :is="'MyCustomPumpChartLine'"
          :itemChart="ChartData"
          :CustomConfig="{
            ...CustomConfig,
            YAxisConfig: ChartConfig.YAxisConfig,
            XAxisConfig: ChartConfig.XAxisConfig,
            XFormatterConfig: Aciveitem.XFormatterConfig,
          }"
          @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun"
          @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun"
          @MyCustomChartMouseMove="MyCustomChartMouseMoveFun"
          @MyCustomChartMouseOut="MyCustomChartMouseOutFun"
          @MyCustomChartMouseClick="MyCustomChartMouseClickFun"
           @MyCustomChartFinished="MyCustomChartFinishedFun"
          @MyCustomChartRendered="MyCustomChartRenderedFun"
        >
      </component>
      <div id="InfoBox"></div>
</div>

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
              show: false,
              symbol: [
                'none',
                'none'
              ],
              symbolSize: [
                10,
                15
              ],
              symbolOffset: [
                0,
                0
              ],
              lineStyle: {
                color: 'red',
                width: 1,
                type: 'solid',
                dashOffset: 0,
                opacity: 1
              }
            },
            AxisTick: {
              inside: false,
              length: 5,
              lineStyle: {
                color: '#222',
                dashOffset: 0,
                opacity: 1,
                type: 'solid',
                width: 1
              },
              show: false
            },
            SplitArea: {
              interval: 'auto',
              show: false,
              areaStyle: {
                color: ['rgba(250,250,250,0.3)', 'rgba(200,200,200,0.3)'],
                opacity: 1,
              }
            },
            SplitLine: {
              show: true,
              lineStyle: {
                type: "solid",
                color: "#333",
                width: 1,
                opacity: 1,
              },
            },
            MinorSplitLine: {
              show: true,
              lineStyle: {
                type: "solid",
                color: "#eee",
                width: 1,
                opacity: 1,
              },
            },
            show: true,
            Name: '',
            MinMax: null
          },
          {
            AxisLabel: {
              Color: 'red',
              IsShow: true,
              FontSize: 12,
              ShowMinLabel: null,
              ShowMaxLabel: null
            },
            AxisLine: {
              show: false,
              symbol: [
                'none',
                'none'
              ],
              symbolSize: [
                10,
                15
              ],
              symbolOffset: [
                0,
                0
              ],
              lineStyle: {
                color: 'red',
                width: 1,
                type: 'solid',
                dashOffset: 0,
                opacity: 1
              }
            },
            AxisTick: {
              inside: false,
              length: 5,
              lineStyle: {
                color: '#222',
                dashOffset: 0,
                opacity: 1,
                type: 'solid',
                width: 1
              },
              show: false
            },
            SplitArea: {
              interval: 'auto',
              show: false,
              areaStyle: {
                color: ['rgba(250,250,250,0.3)', 'rgba(200,200,200,0.3)'],
                opacity: 1,
              }
            },
            SplitLine: {
              show: false,
              lineStyle: {
                type: "solid",
                color: "#333",
                width: 1,
                opacity: 1,
              },
            },
            MinorSplitLine: {
              show: false,
              lineStyle: {
                type: "solid",
                color: "#eee",
                width: 1,
                opacity: 1,
              },
            },
            show: true,
            Name: '',
            MinMax: null
          }
        ],
        XAxisConfig: {
          AxisLine: {
            show: false,
            symbol: [
              'none',
              'none'
            ],
            symbolSize: [
              10,
              15
            ],
            symbolOffset: [
              0,
              0
            ],
            lineStyle: {
              color: 'red',
              width: 10,
              type: 'solid',
              dashOffset: 0,
              opacity: 1
            }
          },
          AxisLabel: {
            Color: 'red',
            IsShow: true,
            FontSize: 12,
            ShowMinLabel: null,
            ShowMaxLabel: null
          },
          AxisTick: {
            inside: false,
            length: 15,
            lineStyle: {
              color: 'red',
              dashOffset: 0,
              opacity: 1,
              type: 'solid',
              width: 1
            },
            show: false
          },

          SplitArea: {
            interval: 'auto',
            show: false,
            areaStyle: {
              color: ['rgba(250,250,250,0.3)', 'rgba(200,200,200,0.3)', 'red'],
              opacity: 1,
            }
          },
          SplitLine: {
            show: true,
            lineStyle: {
              type: "solid",
              color: "#333",
              width: 1,
              opacity: 1,
            },
          },
          MinorSplitLine: {
            show: true,
            lineStyle: {
              type: "solid",
              color: "#eee",
              width: 1,
              opacity: 1,
            },
          },
          show: true,
          Type:"value",// "category",//
          MinMax:null,
          Name: '',

        }
      },
```

```
 :CustomConfig="{
            MarkLineConfig: {
              Padding: [-30, 0, -30, 66],
              SymbolSize: 30,
              FontSize: 12,
              //////
              LabelConfig: {
                Color: 'blue',
                BackGroundColor: '#d6ddee',
                BorderColor: 'blue',
                FontSize: 12,
                BorderWidth: 2,
                BorderRadius: 5,
                Position: 'start',
                Padding: [2, 8, 0, 8],
              },
              ///////
            },
            ScatterConfig: {
              SymbolSize: null,
              SymbolImg: '', //require('./星星.png')
            },
            PolygonDataConfig: {
              TextFillColor: '#333',
              MarkLineFontSize: 16,
              MarkLineWidth: 0,
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
                IsAllSymbol: false,
              },
              TextFontSize: 16,
              SelectConfig: {
                FillColor: '#333',
                StrokeColor: '#D00907',
              },
            },
            DefaultLineConfig: {
              MarkPointDataConfig: {
                LabelFontSize: 12,
                SymbolIcon: 'arrow',
                SymbolSize: 5,
                SymbolColor: 'red',
                SymbolBorderColor: '#222',
                SymbolBorderWidth: 0,
                SymbolBorderType: 'dashed',
                IsLabel: false,
                IsAllSymbol: true,
                //////
                LabelConfig: {
                  Color: 'blue',
                  BackGroundColor: '#d6ddee',
                  BorderColor: 'blue',
                  FontSize: 12,
                  BorderWidth: 2,
                  BorderRadius: 5,
                  Position: 'start',
                  Padding: [2, 8, 0, 8],
                },
                ConnectNulls: true,
                Smooth: true,
                ///////
              },
            },
            YAxisConfig: ChartConfig.YAxisConfig,
            YFormatterConfig: [
              { IsFormatter: true, FormatterValue: 10, Interval: 'auto' },
              { IsFormatter: true, FormatterValue: 10, Interval: 'auto' },
            ],
            XAxisConfig: ChartConfig.XAxisConfig,
            XFormatterConfig: Aciveitem.XFormatterConfig,
            GridConfig: {
              BackGroundColor: '#FFF',
              BorderColor: '#222',
              BorderWidth: 2,
              GridIsShow: true,
            },
            GridFormatterConfig: {
              Left: 60,
              Right: 130,
              Top: 50,
              Bottom: 20,
            },
            TooltipConfig: {
              XAxisName: '流量',
              /////
              AxisPointer: {
                type: 'cross',
                snap: true,
                label: {
                  backgroundColor: 'blue',
                  color: '#fff',

                  lineHeight: 20,
                },

                lineStyle: {
                  color: '#333',
                },
                crossStyle: {
                  color: '#333',
                  width: 1,
                  type: 'dashed',
                },
              },
              Trigger: 'axis',
              Confine: true,
              /////
            },
            LegendConfig: {
              FontSize: 12,
              FontColor: '#6E7B8B',
              Position: 'center', //'right'/'80%'
              Type:"plain"
            },
            GraphicImg: '', //require('./基础数据曲线背景1.png'),
            IsGetDataURL: false,
            /////
            IsMixYAxisConfig: true, //是否使用混合坐标配置模式
            IsMouseMoveOutEvent: true, //是否使用鼠标移入移出事件
            IsClickEvent: true, //是否使用鼠标点击事件
            IsCustomChangeCurveStyle: true, //是否自定义改变曲线样式
            CustomChangeCurveStyleConfig: {
              DefaultColor: '#008702',
              ChangeColor: '#ff8702',
              DefaultMarkPointConfig: {
                itemStyle: {
                  borderColor: '#008702',
                  borderType: 'solid',
                  borderWidth: 0,
                  color: '#008702',
                },
                // symbol: 'circle',
                // symbolSize: 8,
                //...
              },
              ChangeMarkPointConfig: {
                itemStyle: {
                  borderColor: '#ff8702',
                  borderType: 'solid',
                  borderWidth: 0,
                  color: '#ff8702',
                },
                // symbol: 'circle',
                // symbolSize: 8,
                //...
              },
            },
            ///////
          }"
          @MyCustomChartSelectchanged="MyCustomChartSelectchangedFun"
          @MyCustomChartClickGetDataURL="MyCustomChartClickGetDataURLFun"
          @MyCustomChartMouseMove="MyCustomChartMouseMoveFun"
          @MyCustomChartMouseOut="MyCustomChartMouseOutFun"
          @MyCustomChartMouseClick="MyCustomChartMouseClickFun"
           @MyCustomChartFinished="MyCustomChartFinishedFun"
          @MyCustomChartRendered="MyCustomChartRenderedFun"
```

!> itemChart 数据源

!> CustomConfig 自定义配置

```
      CustomConfig//自定义配置：{
                GraphicImg: require('./chart/img/编组 24.png')//背景图片。GraphicImg不配置或者为空时chart背景图片不加载,
                XFormatterConfig: {
                    IsFormatter: true,
                    IsDate: true,
                    FormatterValue: 'h',Interval: 240 }//x轴格式化配置 IsFormatter 是否需要格式化 IsDate 是否是时间 FormatterValue 格式化的条件 如果是时间值为时间格式模板 h或hh 时,mm 分  具体参考：https://echarts.apache.org/zh/option.html#xAxis.axisLabel.formatter, 如果是数字传入数字1,10,100...分别表示取整、保留一位小数、保留二位小数....,
                    Interval 标签间隔 "auto" 自适应 （具体参照Echars官方文档 https://echarts.apache.org/zh/option.html#series-custom.renderItem.return_polygon.x）
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

    //自定义鼠标移入事件
     @MyCustomChartMouseMove="MyCustomChartMouseMoveFun"

      MyCustomChartMouseMoveFun(params) {
      //console.log("MyCustomChartMouseMoveFun事件", params);
      // if (params?.data?.CustomGraphName) {
      //   console.log(
      //     "params.data.CustomGraphName",
      //     params.data.CustomGraphName
      //   );
      // }
      if (params?.data?.CustomInfo?.PumpList) {
        // console.log(
        //   "params.data.CustomInfo",
        //   params.data.CustomInfo
        // );
        debounce(() => {
          this.InitInfoLabelCptClass.DrawFun(params, true);
        }, 100);
      }
    },

    //自定义鼠标移出事件
    @MyCustomChartMouseOut="MyCustomChartMouseOutFun"

    MyCustomChartMouseOutFun(params) {
      // console.log("MyCustomChartMouseOutFun事件", params);
      // if (params?.data?.CustomGraphName) {
      //   console.log(
      //     "params.data.CustomGraphName",
      //     params.data.CustomGraphName
      //   );
      // }
      if (params?.data?.CustomInfo?.PumpList) {
        // console.log(
        //   "params.data.CustomInfo",
        //   params.data.CustomInfo
        // );
        debounce(() => {
          this.InitInfoLabelCptClass.DrawFun(params, false);
        }, 100);
      }
    },

    //自定义鼠标点击事件
    @MyCustomChartMouseClick="MyCustomChartMouseClickFun"

    MyCustomChartMouseClickFun(params) {
      //console.log("MyCustomChartMouseClickFun事件", params);
      // if (params?.data?.CustomGraphName) {
      //   console.log(
      //     "params.data.CustomGraphName",
      //     params.data.CustomGraphName
      //   );
      // }
      // if (params?.data?.CustomInfo?.PumpList) {
      //   console.log(
      //     "params.data.CustomInfo",
      //     params.data.CustomInfo
      //   );
      // }
    },

    
    @MyCustomChartFinished="MyCustomChartFinishedFun"

     MyCustomChartFinishedFun(chart,chartData){
      console.log(`MyCustomChartFinishedFun---chart,chartData`, chart,chartData);
    },

    @MyCustomChartRendered="MyCustomChartRenderedFun"
    
    MyCustomChartRenderedFun(chart,chartData){
      console.log(`MyCustomChartRenderedFun---chart,chartData`, chart,chartData);
    },
```

```
import { InfoLabelCptClass } from "./InfoLabelCpt/index";

  mounted() {
    this.$nextTick(() => {
      this.InitInfoLabelCptClass = new InfoLabelCptClass({});
      this.HandleDataFun(14);
    });
  },
  methods:{
     HandleDataFun(index) {
      import(`./Data/${index}.json`).then((res) => {
        console.log(`res`, res);
        this.ChartData = res.Data;
      });
    },
    MyCustomChartMouseMoveFun(params) {
      //console.log("MyCustomChartMouseMoveFun事件", params);
      // if (params?.data?.CustomGraphName) {
      //   console.log(
      //     "params.data.CustomGraphName",
      //     params.data.CustomGraphName
      //   );
      // }
      if (params?.data?.CustomInfo?.PumpList) {
        // console.log(
        //   "params.data.CustomInfo",
        //   params.data.CustomInfo
        // );
        debounce(() => {
          this.InitInfoLabelCptClass.DrawFun(params, true);
        }, 100);
      }
    },
  }
```
### 自定义信息框

##### InfoLabelCpt/index.js
```
import Vue from "vue";
import LabelCptContainer from "./LabelCpt/index.vue";
let LabelCptVm = Vue.extend(LabelCptContainer);
class InfoLabelCptClass {
    constructor(ParameterConfig) {
        this.ParameterConfig = {
            ...ParameterConfig
        }
        this.InitFun()
    }
    async InitFun() {
        this.ParameterConfig.InfoBox = document.querySelector("#InfoBox"); //获取Dom元素
        this.ParameterConfig.InfoCpt = this.CreateVMInstance({ Title: "InfoLabelCpt" })
        this.ParameterConfig.InfoBox.appendChild(this.ParameterConfig.InfoCpt.$el)
        return this
    }
    // 新建vue组件标签
    CreateVMInstance(Item) {
        let vmInstance = new LabelCptVm({
            propsData: Item
        }).$mount();

        return vmInstance
    }
    DrawFun(params, IsShow) {
        if (IsShow) {
            this.ParameterConfig.InfoCpt.$data.ShowData = params.data.CustomInfo
            this.ParameterConfig.InfoBox.style.display = "block";
            console.log(params, IsShow, this.ParameterConfig.InfoCpt);
            //CanvasHeight CanvasWidth
            let StandRate=90
            if(Math.round(params.event.offsetX/params.CanvasWidth*100)>StandRate){
                this.ParameterConfig.InfoBox.style.left = "unset"
                this.ParameterConfig.InfoBox.style.right = params.GridConfig.Right + "px";
              
            }else{
                this.ParameterConfig.InfoBox.style.right = "unset"
                this.ParameterConfig.InfoBox.style.left = params.event.offsetX + "px";
                
            }
            if(Math.round(params.event.offsetY/params.CanvasHeight*100)>StandRate){
                this.ParameterConfig.InfoBox.style.top = "unset"
                this.ParameterConfig.InfoBox.style.bottom = 10 +params.GridConfig.Bottom+ "px";
            }else{
                this.ParameterConfig.InfoBox.style.bottom = "unset"
                this.ParameterConfig.InfoBox.style.top = params.event.offsetY + 10 + "px";
            }
           
           
        } else {
            console.log("隐藏");
            this.ParameterConfig.InfoBox.style.display = "none";

        }
    }

}
export { InfoLabelCptClass }
```
##### InfoLabelCpt/LabelCpt/index.vue
```
<template>
  <div class="LabelCptContainer" @click="TestFun">
    <div class="ContentOutbox" v-if="ShowData && ShowData.PumpList">
      <div
        v-for="(item, index) in ShowData.PumpList"
        :key="index"
        class="Itembox"
      >
        <div class="ItemInbox">
          {{ item.No }}
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "LabelCptContainer",
  data() {
    return {
      ShowData: {
        Name: "",
        PumpList: [],
      },
    };
  },
  props: {
    Title: {
      type: String,
      default: "标题",
    },
  },
  methods: {
    TestFun() {
      //alert(123)
    },
  },
};
</script>
<style lang="scss" scoped>
.LabelCptContainer {
  cursor: pointer;
  pointer-events: auto;
  background: #212931;
  padding: 5px 10px;
  opacity: 1;
  border: 1px solid #ccc;
  .ContentOutbox {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    align-items: center;

    .Itembox {
      display: flex;
      flex-flow: row nowrap;
      justify-content: center;
      align-items: center;
      width: 24px;
      height: 24px;
      background: #0cc1e0;
      border-radius: 50%;
      margin-right: 5px;
      &:last-child{
        margin-right:0px;
      }
      .ItemInbox {
        font-size: 12px;
        font-family: Digital-7 Mono-Mono, Digital-7 Mono;
        font-weight: 400;
        color: #000;
      }
    }
  }
}
</style>
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

### MyCustomPumpChartLine-Example 实现功能

#### 实现功能 1

![实现功能1](../assets/img/2023-07-22-15-07-08.png ":size=100%")

#### 实现功能 2

![实现功能2](../assets/img/2023-07-22-15-09-03.png ":size=100%")

#### 实现功能 3

![实现功能3](../assets/img/c1.png ":size=100%")
