<template >
    <div class="w-full lg:w-1/2  xl:w-1/3	 md:w-3/4">
        <div class="flex justify-start items-center w-full border-b border-b-black py-2 dark:border-b-white">
            <h1 class="title-contact text-2xl font-semibold">{{isInEnglish?"Let's get in touch":"Mantengámonos en contacto"}}</h1>
        </div>
        <div class="mt-3">
            <form action="https://formsubmit.co/alexsrebernic@gmail.com" method="POST" enctype=”multipart/form-data”>
                <input required type="email" name="email" class="border-b py-3 w-full px-2 dark:bg-gray-700" placeholder="Email">
                <input required type="text" name="_subject" class="border-b py-3 w-full px-2 dark:bg-gray-700" placeholder="Subject">
                <textarea required name="message"  class="border-b w-full mt-3 px-2 py-2 dark:bg-gray-700" id="" cols="30" rows="10" placeholder="Message"></textarea>
                <button type="submit" class="border-2 mt-3 px-6 rounded py-2 text-gray-400 text-md">Send</button>
            </form>
        </div>
        <div class="mt-6 social-media">
            <div class="flex items-center ">
                <a href="https://www.linkedin.com/in/alex-srebernic-201427213/">
                <Icon icon="entypo-social:linkedin-with-circle" width="35px" />
                </a>
                <span class="ml-2">Alex Srebernic</span>
            </div>
              <div class="flex items-center mt-3">
                <Icon icon="ic:sharp-email" width="35px" />
                <span class="ml-2">alexsrebernic@gmail.com</span>
            </div>
              <div class="flex items-center mt-3">
                <a href="https://github.com/alexsrebernic">
                    <Icon class="my-2" icon="akar-icons:github-fill" width="35px"/>
                </a>
                <span class="ml-2">alexsrebernic</span>
            </div>
            <div class="flex items-center mt-3">
                <a href="https://stackoverflow.com/users/17751576/alexsc">
                    <Icon icon="cib:stackoverflow"  width="35px"/>
                </a>
                <span class="ml-2">alexsc_</span>
            </div>
            
        </div>
    </div>
</template>
<script>
export default {
    data(){
       
    },
    props: {
        isInEnglish:Boolean
    },
    components: {
		Icon,
	},
}
import { Icon } from '@iconify/vue';

</script>
<style >
    @import url('https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,400;0,700;1,400;1,700&family=Open+Sans:ital,wght@0,600;0,700;1,500;1,600&display=swap');
    .title-contact{
        font-family: 'Quicksand', sans-serif;
    
    }
    button {
        font-family: 'Quicksand', sans-serif;
        font-weight: 600;
    }

    .social-media span {
        font-family: 'Quicksand', sans-serif;
        font-weight: 600;
    }
    input:focus {
    outline: none;
    }
    textarea {
        outline:none
    }
</style>