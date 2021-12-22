<!--
 * @Date: 2021-12-18 04:26:04
 * @Descripton: 
 * @LastEditTime: 2021-12-23 00:01:36
-->
<script setup>
import { ref, onMounted } from 'vue'
import Background from "../components/Background.vue"
import * as echarts from 'echarts'

let list = [
  {
    policy_country: '工作回顾',
    policy_time: '',
  },
  {
    policy_country: '工作收获',
    policy_time: '',
  },
  {
    policy_country: '个人规划',
    policy_time: '',
  },
  {
    policy_country: '团队建议',
    policy_time: '',
  },
]
let seriesList = []
var yarr = []
var linearr = []
var linev = { value: -0, symbol: 'none' }

list.map((item, index) => {
  seriesList.unshift({
    date: item.policy_time,
    country: item.policy_country,
    value: 0,
    label: {
      show: true,
      lineHeight: 20,
      align: 'left',
      padding: 20,
      position: 'left',
      formatter: function (params) {
        return `{bolder|${params.name}}`
      },
      rich: {
        bolder: {
          fontWeight: 700,
          color: index < 1 ? '#34d399' : '#000',
        },
      },
    },
  })
})
seriesList.map((item, index) => {
  linearr.push({
    value: -0,
  })
  yarr.push(`${item.date}  ${item.country}`)
})
const option = {
  grid: {
    top: 0,
    left: '1%',
    right: '0%',
    bottom: 0,
  },
  legend: {
    bottom: 0,
    itemWidth: 10,
    itemHeight: 10,
    textStyle: {
      padding: [2, 0, 0, 0],
    },
  },
  xAxis: {
    show: false,
    axisLine: { show: false },
    axisTick: { show: false },
    axisLabel: { show: false },
    splitLine: { show: false },
    min: 0,
    max: 0,
  },
  yAxis: {
    type: 'category',
    axisLine: {
      show: true,
      lineStyle: {
        width: 4,
        color: '#34d399',
      },
    },

    axisTick: {
      show: false,
      alignWithLabel: true,
    },
    splitLine: {
      show: false,
    },
    axisLabel: {
      margin: 30,
      alignWithLabel: true,
      show: false,
    },
    data: ['', ...yarr, ''],
  },
  color: ['#34d399'],
  series: [
    {
      type: 'line',
      symbolSize: 8,
      itemStyle: {
        color: '#34d399',
        borderColor: 'red',
        borderWidth: 2,
      },

      hoverAnimation: false,
      legendHoverLink: false,
      data: [linev, ...seriesList, linev],
      lineStyle: {
        color: '#34d399',
      },
    },
  ],
}

const refChart = ref(null)
onMounted(() => {
  // const chart = echarts.init(refChart.value)
  // chart.setOption(option)
  // window.addEventListener("resize", chart.resize())
})
</script>
<template>
  <div class="bg-main slidev-layout">
    <!-- <NavLine /> -->
    <!-- <div ref="refChart" class="chart"></div> -->
    <Background />
    <CornerCurves class="absolute transform bottom-0 right-0 flip-x" />
    <div class="my-auto z-10">
      <slot />
    </div>
  </div>
</template>
<style scoped>
/* .bg-main {
  display: flex;
  justify-content: space-between;
} */
/* .chart {
  position: fixed;
  top: 0;
  left: 0;
  width: 10%;
  height: 100%;
  margin: 0 auto;
} */

</style>
