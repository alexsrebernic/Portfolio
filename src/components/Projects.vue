<template >
    <div class="lg:w-1/2  xl:w-3/6 md:w-3/4">
        <ul>
            <li class="my-3"  v-for="project in arrayProjects" :key="project.id">
                <div class="my-12 pb-6 project-element px-8 xl:flex xl:px-0 border-b">
                    <img class="xl:w-60 " :src="project.image" alt="">
                    <div class="flex flex-col pl-3">
                        <div class="mb-3 border-b">
                            <div class="flex justify-between items-center ">
                                <h1 class="text-center text-2xl  font-bold " v-if="isInEnglish">{{project.nameProjectEnglish}}</h1>
                                <h1 class="text-center text-2xl  font-bold  " v-else>{{project.nameProjectSpanish}}</h1>
                                <a :href="project.githubRepository">
                                    <Icon icon="akar-icons:github-fill" width="25px"/>
                                </a>

                            </div>
                            <a :href="project.pageUrl" class="text-xs text-blue-500 break-all">{{project.pageUrl}}</a>
                        </div>
                        <p v-if="isInEnglish">
                            {{project.detailsEnglish}}
                        </p>
                        <p v-else>  
                            {{project.detailsSpanish}}
                        </p>
                        
                    </div>
                </div>
            </li>
        </ul>
        <div class="flex items-center justify-center flex-col visit-github">
        <span>{{isInEnglish?"To see more of my projects visit my Github":"Para ver todos mis proyectos visita mi Github"}}</span>
        <a href="https://github.com/alexsrebernic">
            <Icon class="my-2" icon="akar-icons:github-fill" width="25px"/>
        </a>
        </div>
    </div>
       
</template>
<script>
export default {
    props:{
        isInEnglish:Boolean
    },
    components: {
		Icon,
	},
    data(){
        return{
            arrayProjects:[
                {
                    id:1,
                    nameProjectEnglish:"Clone Facebook",
                    nameProjectSpanish:"Facebook clon",
                    image:"src/assets/projectsImages/facebook.png",
                    gif:"src/assets/projectsGifs/facebook.gif",
                    githubRepository:"https://github.com/alexsrebernic/Social_Media_TOP",
                    detailsEnglish:"In this application you can register and sign in with the autenticacion of JWT, publish and remove posts, give them like or dislike and add comments to posts. Chat in real time with other people and edit your profile with the technology web sockets, all these interactions are received by a server created by me, i was designed with the architecture REST API. In the Github documentation there are the steps to start it locally and the stack used",
                    detailsSpanish:"En esta aplicacion se puede registrar y iniciar sesion con la autenticacion de JWT, publicar,eliminar,dar like o dislikes y añadir comentarios a posts, mandar mensajes en tiempo real y editar tu perfil con la tecnologia web sockets. Todas estas interacciones las recibe un server creado por mi que fue diseñado con la arquitectura Restful API, en la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado.",
                    pageUrl:"https://condescending-chandrasekhar-2a90a5.netlify.app/"
                },
                 {
                     id:2,
                    nameProjectEnglish:"Clone Coingecko",
                    nameProjectSpanish:"Coingecko clon",
                    image:"src/assets/projectsImages/coingecko.png",
                    gif:"src/assets/projectsGifs/coingecko-clone.gif",
                    githubRepository:"https://github.com/alexsrebernic/Coingecko_Clone_TOP",
                    detailsEnglish:"On this page you can see the price of the first 100 criptocurrency and ther charts,besides the exchanges you can log in with email to mark as favourite your favorite criptocurrency's. To achieve this project, i used the API of Coingecko and the library Chart.js,In the Github documentation there are the steps to start it locally and the stack used  ",
                    detailsSpanish:"En esta pagina se pueden ver el precio de las primeras 100 criptomonedas y sus graficos,ademas de los exchanges,  y se puede iniciar sesion por e-mail para guardar tus criptomonedas favoritas. Para lograr hacer este proyecto se utilizo la API de Coingecko y la libreria Chart.js, en la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado.",
                    pageUrl:"https://alexsrebernic.github.io/Coingecko_Clone_TOP/#/"
                },
                {
                    id:3,
                    nameProjectEnglish:"Cv Creator",
                    nameProjectSpanish:"Cv Creator",
                    image:"src/assets/projectsImages/cv.png",
                    gif:"src/assets/projectsGifs/cv.gif",
                    githubRepository:"https://github.com/alexsrebernic/Cv_Creator_Top",
                    detailsEnglish:"Application to create your resume, contains section for your personal information, education and experience. At the end you can download in PDF, i did this project with React,Bootstrap and the library html2pdf,In the Github documentation there are the steps to start it locally and the stack used",
                    detailsSpanish:"Aplicacion para crear tu curriculum, contiene apartado para tu informacion personal, educacion y experiencia. Al finalizarlo podes descargarlo con pdf, este proyecto lo realize con React,Bootstrap y la libreria html2pdf.En la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado",
                    pageUrl:"https://alexsrebernic.github.io/Cv_Creator_Top/"
                },
                 {
                     id:4,
                    nameProjectEnglish:".todolist",
                    nameProjectSpanish:".todolist ",
                    image:"src/assets/projectsImages/todo-list.png",
                    gif:"src/assets/projectsGifs/to-do.gif",
                    githubRepository:"https://github.com/alexsrebernic/TodoList_TOP",
                    detailsEnglish:"Manage your to-dos and projects with an interactive movement of task and creation of them. Is maded with vanilla Javascript and used the library Calendar.js,In the Github documentation there are the steps to start it locally and the stack used",
                    detailsSpanish:"Administra tus tareas y proyectos con una interactivo movimiento de tareas y creacion de ellas. Fue hecho con vanilla Javascript y se utilizo Calendar.js. En la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado.",
                    pageUrl:"https://alexsrebernic.github.io/TodoList_TOP/"
                },
                 {
                     id:5,
                    nameProjectEnglish:"Etch a sketch",
                    nameProjectSpanish:"Etch a sketch",
                    image:"src/assets/projectsImages/etch-a-sketch.png",
                    gif:"src/assets/projectsGifs/etch-a-sketch.gif",
                    githubRepository:"https://github.com/alexsrebernic/ETCH_A_SKETCH_TOP",
                    detailsEnglish:"Simple web aplication in which you can draw with colors in a frame with configurable extension,when you finish your drawing you can download in png format.In the Github documentation there are the steps to start it locally and the stack used",
                    detailsSpanish:"Simple aplicacion web en la que podes dibujar con colores en un marco con extension configurable, al finalizar tu dibujo este se puede descargar en formato png. En la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado.",
                    pageUrl:"https://alexsrebernic.github.io/ETCH_A_SKETCH_TOP/"
                },
                {
                     id:6,
                    nameProjectEnglish:".members-only",
                    nameProjectSpanish:".members-only",
                    image:"src/assets/projectsImages/members-only.png",
                    gif:"src/assets/projectsGifs/members-only.gif",
                    githubRepository:"https://glacial-reef-98320.herokuapp.com/",
                    detailsEnglish:"Web aplication  consisting in a message board where to publish a message you have to be member,a backend was used with the architecture REST API,In the Github documentation there are the steps to start it locally and the stack used",
                    detailsSpanish:"Aplicacion web que consiste en un tablero de mensajes en el que para publicar un mensaje se debe ser miembro, se utilizo un backend con la arquitectura REST API. En la documentacion de Github estan los pasos para iniciarlo localmente y el stack utilizado.",
                    pageUrl:"https://alexsrebernic.github.io/ETCH_A_SKETCH_TOP/"
                },
                {
                    id:7,
                    nameProjectEnglish:"Portfolio",
                    nameProjectSpanish:"Portafolio",
                    image:"src/assets/projectsImages/portfolio.png",
                    gif:"",
                    githubRepository:"https://github.com/alexsrebernic/Portfolio",
                    detailsEnglish:"This page was made and designed by me, the design was made with Figma and it was used Vue and Tailwind",
                    detailsSpanish:"Esta misma pagina fue diseñada y hecha por mi, el diseño fue hecho en Figma y se utilizo Vue y Tailwind.",
                }
            ]
        }
    }
    
}
import { Icon } from '@iconify/vue';

</script>
<style >
    img {
    image-rendering: auto;
    image-rendering: crisp-edges;

  background-size: contains;
    background-size: cover;
    object-fit:cover;
         		object-position: left;


}
    @import url('https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,400;0,700;1,400;1,700&family=Open+Sans:ital,wght@0,600;0,700;1,500;1,600&display=swap');
    .visit-github {
        font-family: 'Quicksand', sans-serif;
        font-weight: 800;
    }
    .project-element h1{
        font-family: 'Quicksand', sans-serif;
        font-weight: 800;
    }
    .project-element p {
        font-family: 'Merriweather', serif;    
    color: rgba(0, 0, 0, 0.699);
    font-size: 16px;
    line-height: 1.6;
    }
</style>