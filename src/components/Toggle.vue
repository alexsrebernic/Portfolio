<template >
    <div  class="flex items-center justify-end  px-2 py-2 ">
  
  <label for="toggleB" class="flex items-center cursor-pointer ">
      <span class="text-white text-2xl mr-1 dark:text-gray-700">ES</span>
    <!-- toggle -->
    <div  class="relative ">
      <!-- input -->
      <input @click="triggerEventLanguaje" value="true"  type="checkbox" id="toggleB" class="sr-only ">
      <!-- line -->
      <div class="block bg-white w-14 h-8 rounded-full dark:bg-gray-700"></div>
      <!-- dot -->
      <div class="dot absolute left-1 top-1  bg-white w-6 h-6 rounded-full transition dark:bg-gray-600"></div>
    </div>
    <!-- label -->
    <span class="text-white text-2xl ml-1 dark:text-gray-700">EN</span>
  </label>

</div>
</template>
<script>
  export default {
    data(){
      return {
        value: ""
      }
    },
    methods:{
      triggerEventLanguaje(e){
        this.$emit('toggle-languaje')
}
    }
  }
</script>
<style >

    .dot {
        box-shadow: 0px 0px 6px 0px rgba(0,0,0,0.75);
        -webkit-box-shadow: 0px 0px 6px 0px rgba(0,0,0,0.75);
        -moz-box-shadow: 0px 0px 6px 0px rgba(0,0,0,0.75);
    }
    input:checked ~ .dot {
  transform: translateX(100%);
}
</style>