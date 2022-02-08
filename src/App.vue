<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HeaderVue from './components/Header.vue';
import Tabs from './components/Tabs.vue'
</script>
<template>
<div class=" flex justify-start items-center flex-col">
  <HeaderVue/>
  <Tabs/>
</div>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  min-height: 150vh;
}
</style>
