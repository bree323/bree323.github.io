---
theme: ./theme
class: text-center
highlighter: prism
lineNumbers: true
info: |
  ## Slides for Intro to SVG L&L
drawings:
  persist: false
download: true
layout: intro
title: 转正答辩
---

# 转正答辩
>> 答辩人：周源

<div style="margin-top: 20px">
  <span @click="$slidev.nav.next" style="color: #ccc" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    开始 <carbon:arrow-right class="inline"/>
  </span>
</div>


---
layout: presenter
presenterImage: './assets/images/h5.jpg'
---

# 目录

- 🧑‍💻 工作回顾
- 📝 个人收获
- 🎨 个人规划
- 🤹 团队建议

---

# 🧑‍💻 工欲善其事必先利其器

<div class='grid grid-cols-2 grid-rows-1 gap-20'>
  <div>
    <h2 v-click>公司制度学习</h2>
    <ol style="margin: 16px">
      <li v-click>✅ 技术评审流程</li>
      <li v-click>✅ 测试管理流程</li>
      <li v-click>✅ 版本发布流程</li>
      <li v-click>✅ 质量保证流程</li>
    </ol>

  </div>
  <div>
    <h2 v-click>公司相关前端技术栈学习</h2>
    <ol style="margin: 16px">
      <li v-click>✅ react、react-hook、react-router</li>
      <li v-click>✅ mobx</li>
      <li v-click>✅ ramda</li>
      <li v-click>✅ echarts</li>
    </ol>
    <!-- <code>expect(🍚⏱).toYield(✅)</code> -->
  </div>
</div>

---

# 工作回顾 ——> 项目开发
<!-- 
1. 劳务二期
2. 劳务小程序
3. 广州人才大数据（可视化）
4. 疫情防控系统（可视化）
5. 云剑 -->

---
layout: projectDetails
class: text-center
---


# 工作回顾 ——> 组件开发

<!-- <h1>工作回顾 ——> 组件开发</h1> -->
---
layout: componentDetails
class: text-center
---

---

<div class="grid grid-cols-2" style="padding: 24px">
  <figure v-click class="single bg">
        <img class="img-fluid" width="200" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">卡片组件</figcaption>
  </figure>
  <figure v-click class="single bg" style="padding: 24px">
        <img class="img-fluid" width="500" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">人员列表组件</figcaption>
  </figure>
</div>
<p class="p" v-click>
小结： 这两组件基于react类组件的方式实现，开发过程中，遇到组件无条件多次刷新的问题，通过查阅文档以及同事的点拨，对于react类组件的更新机制有了更进一步的理解
</p>

---

<div class="grid grid-cols-1" style="padding: 24px">
  <figure v-click class="single bg">
        <div style="display: flex; justify-content: space-between; width: 100%;">
          <img class="img-fluid" width="300" height="500" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
          <img class="img-fluid" width="300" height="500" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        </div>
        <figcaption class="h2">可配置项表单组件</figcaption>
  </figure>
</div>
<p class="p" v-click>
小结： 采用配置项的方式生成表单项，显著的提高了开发效率，将原本达到上千行的主文件，优化到300到400行之间；这个组件的开发，体会到开发组件中的<b>高内聚低耦合</b>开发思想的重要性。
</p>

---

<div class="grid grid-cols-2" style="padding: 24px">
  <figure v-click class="single bg">
        <img class="img-fluid" width="400" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">类进度条柱状图组件</figcaption>
  </figure>
  <figure v-click class="single bg" style="padding: 24px">
        <img class="img-fluid" width="300" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">饼图组件</figcaption>
  </figure>
</div>

---

<div class="grid grid-cols-2" style="padding: 24px">
  <figure v-click class="single bg">
        <img class="img-fluid" width="400" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">折线图组件</figcaption>
  </figure>
  <figure v-click class="single bg" style="padding: 24px">
        <img class="img-fluid" width="300" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">表格列表组件</figcaption>
  </figure>
</div>
<p class="p" v-click>
小结：数据可视化组件的开发，。
</p>

---

# 工作回顾 ——> 工作总结

  1. 任务分析
    1. 由于对项目没有整体感知，对工时的把控不够
    2. 对ui、ue以及需求文档的审阅不够仔细
  2. bug原因分析：
    1. 优化类
    2. 粗心大意类（错别字、字体、ui取色）
    3. 业务需求类

---

# 个人收获 ——> 技术收获

1. 技术收获
  a. 初步掌握了react技术栈及其生态
  b. 熟悉了小程序的开发
  c. 熟悉了基于ecarts的数据可视化开发
  d. 领悟了低耦合高类聚的组件开发思想
2. 项目开发经验
  a. 开发前需仔细阅读ue及需求文档，对ui整体进行感知后，确定好整体到局部的开发思路后再开发
  b. 界面的组件化开发思想
  c. 采用scss预编译语言，高效编写样式，同时也便于后期的维护
  d. 对于请求返回的数据处理，统一需采用try catch处理，以防数据源的异常导致前端界面报错

---

# 个人规划
## 近期目标
## 长期目标
23
---

# 团队建议
## 我看到的团队
## 我期待的团队

---

# end

<div>end</div>

---
layout: center
class: text-center
---