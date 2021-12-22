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

# 工作回顾
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

<!-- ---

<div class="grid grid-cols-2" style="padding: 24px">
  <figure v-click class="single bg">
        <img class="img-fluid" width="220" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">卡片组件</figcaption>
  </figure>
  <figure v-click class="single bg" style="padding: 24px">
        <img class="img-fluid" width="300" src="https://res.cloudinary.com/kirillkrasin/image/upload/v1529409840/codepen/cat.jpg" alt="image">
        <figcaption class="h2">人员列表组件</figcaption>
  </figure>
</div>
<p class="p" style="position: relative; bottom: 20px" v-click>
<span class="second-color">小结：</span>这两组件基于react类组件的方式实现，开发过程中，遇到组件无条件多次刷新的问题，通过查阅文档以及同事的点拨，对于react类组件的更新机制有了更进一步的理解
</p> -->

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
<span class="second-color">小结：</span>采用配置项的方式生成表单项，显著的提高了开发效率，将原本达到上千行的主文件，优化到300到400行之间；这个组件的开发，体会到开发组件中的<b>高内聚低耦合</b>开发思想的重要性。
</p>

---

<div class="grid grid-cols-2" style="padding: 24px">
  <figure v-click class="single bg">
        <img class="img-fluid" src="/assets/images/pie.jpg" style="with: 220px; height: 130px" alt="image">
        <figcaption class="h2">饼图组件</figcaption>
  </figure>
  <figure v-click class="single bg">
        <img class="img-fluid" src="/assets/images/loop-process-bar.jpg" style="width: 330px; height: 360px; position: relative; right: 50px" alt="image">
        <figcaption class="h2">类进度条柱状图组件</figcaption>
  </figure>
</div>

---

<div class="grid grid-cols-2" style="padding: 24px;">
  <figure v-click class="single bg">
    <img class="img-fluid" style="width: 380px; height: 190px" src="/assets/images/loop-line.jpg" alt="image" />
    <figcaption class="h2">折线图组件</figcaption>
  </figure>
  <figure v-click class="single bg" style="margin-left: 50px">
    <img class="img-fluid" style="width: 300px; height: 320px" src="/assets/images/loop-table.jpg" alt="image" />
    <figcaption class="h2">表格列表组件</figcaption>
  </figure>
</div>
<p class="p" style="width: 47%; position: relative; bottom: 100px" v-click>
  <span class="second-color">小结：</span
  >这些图表组件基于echarts开发，连续经过两个可视化项目的开发，对于echarts的常规配置项已基本掌握；再者，可视化图表对于数据的要求，前端应严谨考虑到数据异常引起的系列问题
</p>

---

# 工作回顾 ——> 总结

|   |     |
| ----- | ------------------- | 
| 任务分析 | <div class="tabletext"> <ol> <li v-click>由于对项目没有整体感知，对工时的把控不够</li> <li v-click>对ui、ue以及需求文档的审阅不够仔细</li> </ol> </div> | 
| bug原因分析 | <div class="tabletext"> <ol> <li v-click>优化类</li> <li v-click>粗心大意类（错别字、字体、ui取色）</li> <li v-click>业务需求类</li> </ol> </div> | 
---

# 个人收获

| 技术收获                | 项目开发经验                                              |
| --------------------- | ------------------------------------------------ |
|  <div class="tabletext"> <ol> <li v-click>基本掌握了<span class="lightHeight">react</span>常用技术栈及其生态</li> <li v-click>熟悉了<span class="lightHeight">小程序</span>的开发</li> <li v-click>界面的<span class="lightHeight">组件化开发</span>思想</li> <li v-click>熟悉了基于ecarts的<span class="lightHeight">数据可视化</span>开发</li> </ol> </div>       |  <div class="tabletext box-p-r-90"> <ol> <li v-click>开发前需仔细阅读<span class="lightHeight">ue</span>及需求文档，对<span class="lightHeight">ui</span>整体进行感知后，确定好整体到局部的开发思路后再开发</li> <li v-click>采用<span class="lightHeight">scss</span>预编译语言，高效编写样式，同时也便于后期的维护</li> <li v-click>领悟了<span class="lightHeight">低耦合高类聚</span>的组件开发思想</li> <li v-click>对于请求返回的数据处理，统一需采用<span class="lightHeight">try catch</span>处理，以防数据源的异常导致前端界面报错</li> </ol></div>                           |

---

# 个人规划

---

<h1>近期规划</h1>

| <span style="font-size: 14px; color: #88ad8f">方向</span>  | <span style="color: #34d399">Typescript</span>     | <span style="color: #34d399">可视化</span>      |    <span style="color: #34d399">深入项目常规技术栈</span>                               |
| ---- | -------------- | ---------------- | ---------------------------------- |
| <span style="font-size: 14px; color: #88ad8f">目标</span>  | <div class="tabletext" v-click>组件采用Typescript开发</div>      | <div class="tabletext" v-click>熟悉掌握相关技术栈： echart\svg\canvas</div>  |  <div class="tabletext box-p-r-90"> <ol> <li v-click>进一步掌握react-hooks、mobx的使用及原理；</li> <li v-click>react-router缺少实际开发应用，在项目中进一步掌握</li> <li v-click>进一步熟悉ramda中常用api</li> </ol> </div>            |

---
layout: longPlan
class: text-center
---

---
# 团队建议

---
<h1>团队建设</h1>

|     | 团队优势     | 建议                                              |
| --- | --------- | ---------------------------------------------------------- |
| 1.  |  <div v-click class="tabletext" style="padding-right: 20px">公司的<a href="http://doc.d-bigdata.com:18888/docs/web/web-1cjsl7riha85a">在线文档</a>给技术分享提供了一个平台，我们可以在这个平台上实现技术积累</div>    | <div v-click class="tabletext box-p-r-90"><span style="color: #88ad8f">不足：</span>由于项目任务繁重，互动性上和积极性上较为缺乏 <br/> <span style="color: #34d399">建议：</span> 在<a href="https://www.yuque.com/codingfor/sum/gyn1cv#LZptPY1MvlZXXxGKO9Wgmg1QU4aHLk8x">语雀</a>上创建一个知识小组或者协作知识库，提高大家在技术交流上的积极性</div>                           |
| 2.  | <div v-click class="tabletext"> 前端团队拥有可视化组件图表预览库<a href="http://42.123.99.90:29999/#/">FFun-components-viewer</a></div>                         | <div v-click class="tabletext box-p-r-90"><span style="color: #88ad8f">不足：</span> 仅提供了预览作用，可操作性并不理想 <br/> <span style="color: #34d399">建议：</span>针对基于echarts的组件，可在echarts提供的<a href="https://www.makeapie.com/user.html?u=obd-o-6S8d0eJw6Pc3GW1rgYuU54gexNDAm&type=star">组件平台</a>共享，提高可视化组件的开发效率</div>                              |
| 3.  |  <div v-click class="tabletext">雄厚的技术实力</div>          |  <div v-click class="tabletext box-p-r-90">不定期进行codeReview</div>               |
