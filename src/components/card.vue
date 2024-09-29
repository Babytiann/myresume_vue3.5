<script setup>
const card_class = defineProps({
  name: String
})

</script>

<template>
  <section class="educator">
    <span class="title-large">教育经历</span>
    <div class="card">
      <div class="list-item-header">
        <div class="logobox">
          <img class="logo" src="../img/西财大logo.jpg" alt="西安财经大学的logo">
        </div>
        <div class="name-time">
          <span class="name">西安财经大学</span>
          <span class="time">2023.09-2027.06</span>
        </div>
      </div>
    </div>
  </section>
  <section class="experience">
    <span class="title-large">实习经历</span>
    <div class="card">

      <div class="list-item-content">
                        <span class="title-s">
                            <b>暂无</b>
                        </span>
      </div>
    </div>           <!--这个card类是一个模板，以后添加元素都可以直接使用-->
  </section>
  <section class="project">
    <span class="title-large">项目经历</span>
    <div class="card">
      <div class="list-item-content">
        <span class="title-s">
          <b>暂无</b>
        </span>
      </div>
    </div>
  </section>
  <section class="tecnology">
    <span class="title-large">比赛经历</span>
    <ul>
      <li>2024年蓝桥杯省级二等奖</li>
    </ul>
  </section>
  <section class="tecnology">
    <span class="title-large">技术储备</span>
    <ul>
      <li>熟悉python, HTML,C++,JS等多门编程语言的编写,对面向对象编程思想和设计模式有深刻理解。</li>
      <li>熟悉，掌握图论、数论部分知识以及多种算法如，dfs，bfs，最短路径规划，线段树</li>
      <li>熟悉git等版本控制工具的使用</li>
    </ul>
  </section>
</template>

<style scoped>
.title-large{
  margin-bottom: 20px;
  font-size: var(--title-little-size);
  font-weight: var(--title-weight);
  float: left;
  padding: 16px;
  color: var(--body-font-color);
}
.card{
  overflow: hidden;
  color: var(--body-font-color);
  background-color: var(--body-bg-color);
  border-radius: var(--all-border-radius);
  border: 1px solid var(--all-outline-color1);
  padding: 24px;
  line-height: 1.8;
}
.list-item-header{
  display: flex;
  align-items: center;
  gap: 16px;
}

.logobox{
  width: 40px;
  height: 40px;
  min-width: 40px;
  min-height: 40px;     /*设置头像的大小,并且防止了当视口特别小的时候图像消失*/
}
.logo{
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: contain;  /*设置头像的样式,与上面一样都是模板*/
}
.name-time{
  display: grid;
  grid-template-rows: repeat(2, 1fr);
  font-size: var(--body-name-font-size);
  gap: 1px;           /*介绍这个logo的公司名字以及时间*/
}

main section{
  margin-top: 50px;
}
.title-s{
  font-weight: var(--title-weight);
  font-size: 1.25em;        /*每个card里面的主要内容的小标题*/
}
ul{
  list-style-type: circle;   /*每个card里面的主要的列表*/
  padding-left: 20px;
}


@page {
  margin: 0;
}

body {
  margin: 1cm; /* 你可以调整这个值来确保页面内容不会紧贴页面边缘 */
}

.project,.tecnology{
  page-break-inside: avoid;  /*避免在这两个类里面分页,让他们都出现在一张纸上*/
}
</style>