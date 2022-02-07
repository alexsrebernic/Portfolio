
<template>
    <header>
        <div class="hero css-selector flex justify-end items-start">
            <Toggle/>
        </div>
        <div class="flex flex-col items-center">
            <div class=" rounded-full w-52 h-52 bg-white absolute image-header flex items-center justify-center">
                <img class="rounded-full w-48 h-48 object-left" src="" alt="">
            </div>
        </div>
    </header>
</template>
<script>
import Toggle from './Toggle.vue'
export default {
    name:'App',
    components: {
        Toggle
    }
}
</script>
<style >
    .image-header {
        transform: translateY(-104px);
    }
    .hero {
        height: 25vh;
    }
    .css-selector {
    background: linear-gradient(270deg, #b479ee, #7294ea, #77d0ea, #79e8c2);
    background-size: 800% 800%;

    -webkit-animation: AnimationName 23s ease infinite;
    -moz-animation: AnimationName 23s ease infinite;
    -o-animation: AnimationName 23s ease infinite;
    animation: AnimationName 23s ease infinite;
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
    @-o-keyframes AnimationName {
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