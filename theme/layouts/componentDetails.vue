<!--
 * @Date: 2021-12-19 17:09:35
 * @Descripton: 
 * @LastEditTime: 2021-12-20 22:43:03
-->
<script setup>
import { ref, onMounted } from 'vue'
import * as echarts from 'echarts'

const xData = ['劳务二期', '劳务小程序', '广州人才大数据', '疫情防控管理平台']
const yData = [2, 1, 4, 3]
const option = {
  // backgroundColor: '#061326',
  grid: {
    top: '25%',
    left: '-5%',
    bottom: '5%',
    right: '5%',
    containLabel: true,
  },
  title: {
    show: false,
    text: 'Main Title',
    subtext: 'Sub Title',
    left: 'center',
    top: '30',
    textStyle: {
      fontSize: 30,
    },
    subtextStyle: {
      fontSize: 20,
    },
  },
  tooltip: {
    show: true,
  },
  animation: false,
  xAxis: [
    {
      type: 'category',
      data: xData,
      axisTick: {
        alignWithLabel: true,
      },
      nameTextStyle: {
        color: '#82b0ec',
      },
      axisLine: {
        show: false,
        lineStyle: {
          color: '#82b0ec',
        },
      },
      axisLabel: {
        textStyle: {
          color: '#fff',
        },
        margin: 30,
      },
    },
  ],
  yAxis: [
    {
      show: false,
      type: 'value',
      axisLabel: {
        textStyle: {
          color: '#fff',
        },
      },
      splitLine: {
        lineStyle: {
          color: '#0c2c5a',
        },
      },
      axisLine: {
        show: false,
      },
    },
  ],
  series: [
    {
      name: '',
      type: 'pictorialBar',
      symbolSize: [40, 10],
      symbolOffset: [0, -6],
      symbolPosition: 'end',
      z: 12,
      // "barWidth": "0",
      label: {
        normal: {
          show: true,
          position: 'top',
          // "formatter": "{c}%"
          fontSize: 15,
          fontWeight: 'bold',
          color: '#34DCFF',
        },
      },
      color: '#2DB1EF',
      data: yData,
    },
    {
      name: '',
      type: 'pictorialBar',
      symbolSize: [40, 10],
      symbolOffset: [0, 7],
      // "barWidth": "20",
      z: 12,
      color: '#2DB1EF',
      data: yData,
    },
    {
      name: '',
      type: 'pictorialBar',
      symbolSize: [50, 15],
      symbolOffset: [0, 12],
      z: 10,
      itemStyle: {
        normal: {
          color: 'transparent',
          borderColor: '#2EA9E5',
          borderType: 'solid',
          borderWidth: 1,
        },
      },
      data: yData,
    },
    {
      name: '',
      type: 'pictorialBar',
      symbolSize: [70, 20],
      symbolOffset: [0, 18],
      z: 10,
      itemStyle: {
        normal: {
          color: 'transparent',
          borderColor: '#19465D',
          borderType: 'solid',
          borderWidth: 2,
        },
      },
      data: yData,
    },
    {
      type: 'bar',
      //silent: true,
      barWidth: '40',
      barGap: '10%', // Make series be overlap
      barCateGoryGap: '10%',
      itemStyle: {
        normal: {
          color: new echarts.graphic.LinearGradient(0, 0, 0, 0.7, [
            {
              offset: 0,
              color: '#38B2E6',
            },
            {
              offset: 1,
              color: '#0B3147',
            },
          ]),
          opacity: 0.8,
        },
      },
      data: yData,
    },
  ],
}

const refChart1 = ref(null)
// const refChart2 = ref(null)
onMounted(() => {
  const chart1 = echarts.init(refChart1.value)
  // const chart2 = echarts.init(refChart2.value)
  chart1.setOption(option)
  // chart2.setOption(option2)
})
</script>

<template>
  <div class="bg-main slidev-layout">
    <div class="background">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>
    <CornerCurves class="absolute transform bottom-0 right-0 flip-x" />
    <div class="my-auto z-10">
      <h1 style="width: 50px; text-align: center; height: 50px">
        组件开发统计
      </h1>
      <!-- <div class="img"></div> -->
      <div ref="refChart1" class="chart"></div>
      <!-- <div ref="refChart2" class="chart"></div> -->
    </div>
  </div>
</template>
<style scoped>
.bg-main {
  width: 100%;
  height: 100%;
}
.my-auto {
  position: relative;
  /* bottom: 50px; */
  width: 100%;
  height: 100%;
  min-height: 500px;
  display: flex;
  justify-content: space-between;
}
.img {
  width: 30%;
  height: 100%;
  background-image: url('../public/images/h1.jpg');
  background-size: contain;
  background-repeat: no-repeat;
}
.chart {
  width: 60%;
  height: 85%;
  margin: 0 auto;
}

</style>
