<!--
 * @Date: 2021-12-19 17:09:35
 * @Descripton: 
 * @LastEditTime: 2021-12-20 00:42:34
-->
<script setup>
import { ref, onMounted } from 'vue'
import * as echarts from 'echarts'

let list = [
  {
    policy_country: '工作回顾',
    policy_time: 'step1',
  },
  {
    policy_country: '工作收获',
    policy_time: 'step2',
  },
  {
    policy_country: '中国',
    policy_time: '2007-06-22',
  },
  {
    policy_country: '中国',
    policy_time: '2016-02-06',
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
  const chart = echarts.init(refChart.value)
  chart.setOption(option)
})
</script>

<template>
  <div ref="refChart" class="chart"></div>
</template>

<style scoped>
.chart {
  position: fixed;
  top: 0;
  left: 0;
  width: auto;
  height: 100%;
  margin: 0 auto;
}
</style>
