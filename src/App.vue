<script setup>
import selfHead from './components/Head.vue'
import card from './components/card.vue'
import { reactive } from "vue";

const classArray = reactive({
  name : "education",

})

</script>

<template>
  <div class="container">
    <header>
      <self-head></self-head>
    </header>
    <main>
      <card v-bind = "classArray"></card>
    </main>
  </div>

</template>

<style scoped>

</style>
