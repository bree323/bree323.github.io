<!--
 * @Date: 2021-12-18 04:26:04
 * @Descripton: 
 * @LastEditTime: 2021-12-20 02:00:17
-->
<script setup>
import { ref, onMounted } from 'vue'
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
    <div class="background">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>
    <!-- <NavLine /> -->
    <!-- <div ref="refChart" class="chart"></div> -->

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


@keyframes move {
    100% {
        transform: translate3d(0, 0, 10px) rotate(360deg);
    }
}

.background {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    background: #37495b;
    overflow: hidden;
}

.background span {
    width: 6vmin;
    height: 6vmin;
    border-radius: 6vmin;
    backface-visibility: hidden;
    position: absolute;
    animation: move;
    animation-duration: 15;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
}


.background span:nth-child(0) {
    color: #798b79;
    top: 43%;
    left: 61%;
    animation-duration: 42s;
    animation-delay: -35s;
    transform-origin: 20vw -3vh;
    box-shadow: 26vmin 0 4.240864332035349vmin currentColor;
}
.background span:nth-child(1) {
    color: #798b79;
    top: 15%;
    left: 9%;
    animation-duration: 49s;
    animation-delay: -7s;
    transform-origin: 25vw 21vh;
    box-shadow: -26vmin 0 3.5346833844227388vmin currentColor;
}
.background span:nth-child(2) {
    color: #426f6a;
    top: 40%;
    left: 5%;
    animation-duration: 53s;
    animation-delay: -46s;
    transform-origin: 4vw -1vh;
    box-shadow: -26vmin 0 3.6407130369871004vmin currentColor;
}
.background span:nth-child(3) {
    color: #798b79;
    top: 64%;
    left: 29%;
    animation-duration: 41s;
    animation-delay: -20s;
    transform-origin: -19vw -2vh;
    box-shadow: -26vmin 0 4.033018428420929vmin currentColor;
}
.background span:nth-child(4) {
    color: #426f6a;
    top: 42%;
    left: 100%;
    animation-duration: 54s;
    animation-delay: -47s;
    transform-origin: -16vw -14vh;
    box-shadow: 26vmin 0 3.9086947077707235vmin currentColor;
}
.background span:nth-child(5) {
    color: #426f6a;
    top: 15%;
    left: 69%;
    animation-duration: 39s;
    animation-delay: -30s;
    transform-origin: -15vw -24vh;
    box-shadow: 26vmin 0 3.7711318392218875vmin currentColor;
}
.background span:nth-child(6) {
    color: #426f6a;
    top: 67%;
    left: 32%;
    animation-duration: 8s;
    animation-delay: -47s;
    transform-origin: -22vw -3vh;
    box-shadow: 26vmin 0 4.182789151774853vmin currentColor;
}

</style>
