<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { ref } from '@vue/reactivity';
import HeaderVue from './components/Header.vue';
import Tabs from './components/Tabs.vue'
  let isInEnglish = ref(false)

   function toggleLanguaje(){
            if(isInEnglish.value){
                isInEnglish.value = false
            } else {
                isInEnglish.value = true
            }
            console.log(isInEnglish.value)
        }
</script>
<template>
<div class=" flex justify-start items-center flex-col">
  <HeaderVue :isInEnglish="isInEnglish" @toggle-languaje="toggleLanguaje" />
  <Tabs :isInEnglish="isInEnglish"/>
  <div class="flex items-start w-full">
    <span class="text-gray-400 text-md footer-text">Alex Srebernic 2022 ©</span>
  </div>
</div>
</template>

<style>
.footer-text {
        font-family: 'Merriweather', serif;    

}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  min-height: 100vh;
}
</style>
