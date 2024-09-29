<script setup>
  import {ref} from "vue";

  const idRef = ref("id")
  const email = ref("2413915435@qq.com")
  const href_email = ref(`mailto:${email}`)
  const phonenum = ref("18367032932")
  const href_phonenum = ref(`tel:${phonenum}`)
</script>

<template>
  <div class="pre-head">
    <div class="switch-icon"><img src="../img/切换语言图标.png" alt="切换语言图标" title="click here to switch language in English" /></div>
    <div class="print-icon"><img src="../img/打印.png" alt="打印图标" title="点击打印" /></div>
  </div>
  <section>
    <span :class="idRef">翻斗幼儿园甜甜</span>
    <div class="header-div">
      <div class="mail">
        <a :href="href_email" class="header-a" title="点击发送邮件">
          <span><img src="../img/图标-邮件.png" alt="邮箱" /></span>
          <span class="up">{{ email }}</span>
        </a>
      </div>
      <div class="phone">
        <a :href="href_phonenum" class="header-a">
          <span><img src="../img/图标-电话.png" alt="电话" /></span>
          <span class="up">(+86) {{ phonenum }}</span>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.pre-head{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.print-icon, .switch-icon{
  width: 30px;
  height: auto;
}
.print-icon img, .switch-icon img{
  width: 30px;
  height: auto;
  object-fit: contain;
  cursor: pointer;
}

header section{
  margin-top: 25px;
  background-color: var(--header-bg-color);
  padding: 24px 16px 32px;
  border-radius: var(--all-border-radius);
  border:1px solid var(--all-outline-color1);
}                              /*设置头部的样式*/

.id{
  font-weight: var(--title-weight);
  font-size: var(--title-large-size);
  padding: 16px;
}                               /*设置头部的标题样式*/

.header-div{
  display: flex;
  align-items: center;
  padding:16px 16px 0;
  gap: 16px;
}                              /*设置头部的div样式，形成flex布局，让那几个图标依次排开*/

.header-div div{
  border: 1px solid var(--all-outline-color2);
  background-color: var(--header-bg-secondary-color);
  border-radius: var(--all-border-radius);
  height: 32px;
  padding: 5px 8px;
}                             /*控制图标位置，以及每一块超链接的样式*/

.header-div div img{
  width: 18px;
  height: auto;
  object-fit: contain;
}                            /*控制图标的大小*/

.header-a{
  display: flex;
  align-items: center;
  gap: 8px;
}                             /*控制内部样式，以免文字跟图标不平齐，下面的.up也是*/

.up{
  position:relative;
  bottom: 2.3px;
}

@media print{
  .pre-head{
    display: none;        /*打印时隐藏头部的图标*/
  }
}

</style>