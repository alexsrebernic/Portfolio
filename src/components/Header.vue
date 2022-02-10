
<template>
    <header class="w-full 2xl:w-4/5  ">
        <div class="hero shadow-xl css-selector flex justify-end items-start 2xl:rounded-b-md">
            <Icon v-if="isInDarkMode" icon="akar-icons:sun" width="30px" class="mt-2 cursor-pointer" @click="toggleDarkMode" color="dark" />
            <Icon v-else  icon="bx:bxs-moon" color="white" width="35px" class="mt-1 cursor-pointer" @click="toggleDarkMode"/>
            <Toggle @toggle-languaje="triggerEventLanguaje"/>
        </div>
        <div class="flex flex-col items-center">
            <div class=" rounded-full dark:bg-gray-700 w-52 h-52 bg-white  absolute image-header flex items-center justify-center">
                <img class="rounded-full shadow-xl w-48 h-48 object-left" src="../assets/Screenshot from 2022-02-07 17-25-08.png" alt="">
            </div>
          
        </div>
        <div class="flex justify-center items-center dark:bg-gray-700">
          <div class="inline-flex items-center justify-center flex-col mt-28 border-b pb-2 px-6">
                <div>
                <h1 class="text-5xl truncate font-sm text-center dark:text-white">Alex Srebernic</h1>
                <h1  class="text-xl truncate font-semibold mt-3 text-center text-gray-500 dark:text-gray-300">{{isInEnglish?"Full-stack web developer":"Desarrollador web Full-stack"}}</h1>
                </div>
            </div>
        </div>
    </header>
</template>
<script>
import Toggle from './Toggle.vue'
export default {
    name:'App',
    data(){
        return{
            isInEnglish:false,
            isInDarkMode:false
        }
    },
    props: {
        isInEnglish:Boolean
    },
    methods:{
         triggerEventLanguaje(e){
        this.$emit('toggle-languaje')
       
    },
    toggleDarkMode(){
        if (localStorage.theme === 'dark' ) {
            localStorage.removeItem("theme")
            this.isInDarkMode = false
            document.documentElement.classList.remove('dark')
        } else if(!('theme' in localStorage)){
        document.documentElement.classList.add('dark')
        this.isInDarkMode = true
        localStorage.setItem("theme","dark")
        }
    }
    },
    components: {
        Toggle,
        Icon,

    }
}
import { Icon } from '@iconify/vue';

</script>
<style >
    @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');    
    header {
        font-family: 'Quicksand', sans-serif;
    }
   
    .image-header {
        transform: translateY(-104px);
    }
    .hero {
        height: 25vh;
    }
.css-selector {
    background: linear-gradient(270deg, #7930aa, #604ad7, #5894d9, #70d2dd, #4be386, #9ff76d, #d7f55c, #f5d05c, #f58d5c, #f55c5c, #f55ce2);
    background-size: 2200% 2200%;

    -webkit-animation: AnimationName 30s ease infinite;
    -moz-animation: AnimationName 30s ease infinite;
    animation: AnimationName 30s ease infinite;
}

@-webkit-keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
@-moz-keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
@keyframes AnimationName {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}

   
</style>