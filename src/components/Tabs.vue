<template>
  <div class="w-full dark:bg-gray-700">
    <div class="w-full">
        <div class="flex justify-center items-center">
      <ul class="flex  list-none  pt-3 pb-4 m-0 items-center justify-center w-4/5">
      
        <li class=" px-4 text-center">
          <span class=" one text-tabs truncate   py-3  cursor-pointer dark:text-white" v-on:click="toggleTabs(1)" v-bind:class="{ 'activespan': openTab === 1}">
            {{isInEnglish?"About me":"Acerca de mi"}}
          </span>
        </li>
        <li class=" px-4 text-center">
          <span class=" two text-tabs truncate   py-3   cursor-pointer dark:text-white" v-on:click="toggleTabs(2)" v-bind:class="{'activespan': openTab === 2}">
          {{isInEnglish?"Projects":"Proyectos"}}

          </span>
        </li>
        <li class=" px-4 text-center">
          <span class=" text-tabs three truncate    py-3   cursor-pointer dark:text-white" v-on:click="toggleTabs(3)" v-bind:class="{'activespan': openTab === 3}">
            {{isInEnglish?"Contact me":"Contactame"}}
          </span>

        </li>
      </ul>

      </div>
      <div class=" flex flex-col min-w-0  bg-white w-full  mt-8">
        <div class="px-4 py-5 dark:bg-gray-700">
          <div class="dark:text-white">
            <div v-bind:class="{'hidden': openTab !== 1, 'flex items-center justify-center': openTab === 1}">
              <AboutMe :isInEnglish="isInEnglish"/>
            </div>
            <div v-bind:class="{'hidden': openTab !== 2, 'flex items-center justify-center': openTab === 2}">
              <Projects :isInEnglish="isInEnglish"/>
            </div>
            <div v-bind:class="{'hidden': openTab !== 3, 'flex items-center justify-center': openTab === 3}">
              <ContactMe :isInEnglish="isInEnglish"/>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            openTab: 1,
        };
    },
    name: "pink-tabs",
    props: {
        isInEnglish: Boolean
    },
    methods: {
        toggleTabs: function (tabNumber) {
            this.openTab = tabNumber;
        }
    },
  
   
    components: { AboutMe, Projects, ContactMe }
}
import { toRefs } from "vue";
import AboutMe from "./AboutMe.vue"
import Projects from "./Projects.vue";
import ContactMe from './ContactMe.vue'
</script>
<style >
    @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');    
    .text-tabs {
      font-size: 16px;
      font-weight: 500;
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
    .text-tabs:hover,
    .text-tabs:focus,
    .text-tabs:active {
      background-size: 100% 0.1em;
    }
    .activespan {
      background-size: 100% 0.1em;

    }
</style>