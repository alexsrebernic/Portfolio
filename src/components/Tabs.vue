<template>
  <div class="flex flex-wrap">
    <div class="w-full">
        <div class="flex justify-center items-center">
      <ul class="flex  list-none  pt-3 pb-4 m-0 items-center justify-center w-4/5">
      
        <li class="-mb-px  last:mr-0 px-6 text-center">
          <span class="text-xs one truncate  text-lg  py-3  cursor-pointer" v-on:click="toggleTabs(1)" v-bind:class="{ 'activespan': openTab === 1}">
            About me
          </span>
        </li>
        <li class="-mb-px  last:mr-0 px-6 text-center">
          <span class="text-xs two truncate  text-lg  py-3   cursor-pointer" v-on:click="toggleTabs(2)" v-bind:class="{'activespan': openTab === 2}">
            Projects
          </span>
        </li>
        <li class="-mb-px last:mr-0 px-6 text-center">
          <span class="text-xs three truncate  text-lg  py-3   cursor-pointer" v-on:click="toggleTabs(3)" v-bind:class="{'activespan': openTab === 3}">
            Contact me
          </span>

        </li>
      </ul>

      </div>
      <div class=" flex flex-col min-w-0  bg-white w-full  ">
        <div class="px-4 py-5 ">
          <div class="tab-content tab-space">
            <div v-bind:class="{'hidden': openTab !== 1, 'block': openTab === 1}">
            
            </div>
            <div v-bind:class="{'hidden': openTab !== 2, 'block': openTab === 2}">
           
            </div>
            <div v-bind:class="{'hidden': openTab !== 3, 'block': openTab === 3}">
           
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "pink-tabs",
  data() {
    return {
      openTab: 1
    }
  },
  methods: {
    toggleTabs: function(tabNumber){
      this.openTab = tabNumber
    }
  }
}
</script>
<style >
    @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');    
    span {
        font-family: 'Quicksand', sans-serif;
          text-decoration: none;
           background-image: linear-gradient(#d1d3d6, #dfdddb);
            background-size: 0% 0.1em;
            background-position-y: 100%;
            background-position-x: 0%;
            background-repeat: no-repeat;
            transition: background-size 0.2s ease-in-out;
            text-decoration: none;
    }
    span:hover,
    span:focus,
    span:active {
      background-size: 100% 0.1em;
    }
    .activespan {
      background-size: 100% 0.1em;

    }
</style>