
<template>
    <header class="w-full 2xl:w-4/5  ">
        <div class="hero shadow-xl css-selector flex justify-end items-start 2xl:rounded-b-md">
            <Toggle @toggle-languaje="toggleLanguaje"/>
        </div>
        <div class="flex flex-col items-center">
            <div class=" rounded-full w-52 h-52 bg-white xl absolute image-header flex items-center justify-center">
                <img class="rounded-full shadow-md w-48 h-48 object-left" src="../assets/Screenshot from 2022-02-07 17-25-08.png" alt="">
            </div>
          
        </div>
        <div class="flex justify-center items-center">
          <div class="inline-flex items-center justify-center flex-col mt-28 border-b pb-2 px-6">
                <div>
                <h1 class="text-5xl truncate font-sm text-center">Alex Srebernic</h1>
                <h1 class="text-xl truncate font-semibold mt-3 text-center">Full-stack web developer</h1>
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
            isInSpanish:true
        }
    },
    methods:{
        toggleLanguaje(){
            if(this.isInSpanish){
                this.isInSpanish = false
                this.isInEnglish = true
            } else if(this.isInEnglish){
                this.isInEnglish = false
                this.isInSpanish = true
            }
            console.log(this.isInEnglish,this.isInSpanish)
        }
    },
    components: {
        Toggle
    }
}
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
    background: linear-gradient(270deg, #6f23a3, #6169db, #61b4db, #66cbd5);
    background-size: 800% 800%;

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