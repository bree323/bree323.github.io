<!--
 * @Date: 2021-12-23 01:13:33
 * @Descripton: 
 * @LastEditTime: 2021-12-23 01:13:34
-->
<template>
  <div class="grid grid-cols-2" style="padding: 24px">
    <figure v-click class="single bg">
      <img class="img-fluid" width="400" src="../../assets/images/loop-line.jpg" alt="image" />
      <figcaption class="h2">折线图组件</figcaption>
    </figure>
    <figure v-click class="single bg" style="padding: 24px">
      <img class="img-fluid" width="300" src="../../assets/images/loop-table.jpg" alt="image" />
      <figcaption class="h2">表格列表组件</figcaption>
    </figure>
  </div>
  <p class="p" v-click>
    <span class="second-color">小结：</span
    >这些图表组件基于echarts开发，连续经过两个可视化项目的开发，对于echarts的常规配置项已基本掌握；再者，可视化图表对于数据的要求，前端应严谨考虑到数据异常引起的系列问题
  </p>
</template>
