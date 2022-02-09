<template >
    <div class="text-lg lg:w-1/2  xl:w-2/6 md:w-3/4">
      <div v-if="isInEnglish" class="about-me-element px-2 ">
                <h1 class="title-about-me text-3xl mb-6 font-semibold">About me</h1>
          <p class="text-about ">
                Welcome! My name is Alex Srebernic and i'm a and I am a self-taught web developer, i am currently 17 years old and i live in Neuquen, Argentina.   
          </p>
          <p>
               I started studying web development  {{dateInEnglish}} and during all this time I have learned  libraries and frameworks both frontend <span class="text-sm">(React,Vue)</span>  and  Backend <span class="text-sm">(Express,Rest API,Node.js,Web sockets,MongoDB,Firebase,etc)</span>. 
          </p>
          <p class="text-about">
                All this knowledge was acquired by the web,thanks to the excellent resources provided  by web courses like <a class="cursor-pointer underline text-blue-600" href="https://www.theodinproject.com/">The odin project</a> , <a class="cursor-pointer underline text-blue-600" href="https://www.freecodecamp.org/">Freecodecamp</a> and Harvard's CS50. In them i learned the fundamentals and basics of the internet.
              
            </p> 
            <p class="text-about">
                  I consider myself a person highly  <span class="font-bold">disciplined</span> and retailed  , able to adapt and learn any technology. I enjoy learning, creating and collaborating with people on projects, apart from programming, I also like to practice calisthenics, read books and the nature.
            </p>
          <h1 class="title-about-me text-3xl my-6 font-semibold">Present</h1>
            <p>
                At the present time i'm working in the backend of a cryptocurrency courses page with Firebase, i keep studying and searching for a position for junior web developer where i can be part of a teamwork. In which i can continue to have a personal and professional growth.
            </p>
      </div>
      <div class="about-me-element px-2" v-else>
          <h1 class="title-about-me text-3xl mb-6 font-semibold">Acerca de mi</h1>
          <p class="text-about">
                ¡Bienvenido! Me llamo Alex Srebernic y soy un desarrollador web autodidacta,actualmente tengo 17 años y vivo en Neuquen, Argentina.   
          </p>
          <p>
               Empeze a estudiar desarrollo web hace mas de {{dateInSpanish}} y durante todo este tiempo e aprendido librerias y marcos de trabajo tanto Frontend <span class="text-sm">(React,Vue)</span>  como  Backend <span class="text-sm">(Express,Rest API,Node.js,Web sockets,MongoDB,Firebase,etc)</span>. 
          </p>
          <p class="text-about">
                Todo este conocimiento lo e adquirido por internet,gracias a los excelentes recursos proveidos  por cursos web como <a class="cursor-pointer underline text-blue-600" href="https://www.theodinproject.com/">The odin project</a> , <a class="cursor-pointer underline text-blue-600" href="https://www.freecodecamp.org/">Freecodecamp</a>,<a class="cursor-pointer underline text-blue-600" href="https://platzi.com/">Platzi</a> y Harvard's CS50. En ellos aprendi los fundamentos y bases de la web.
            </p> 
            <p class="text-about">
                  Me considero una persona altamente <span class="font-bold">disciplinada</span> y detallista  , capaz de adaptarse y aprender cualquier tecnologia. Disfruto de aprender , crear y  colaborar con personas en proyectos, aparte de la programacion tambien me gusta practicar calistenia, leer libros y la naturaleza.
            </p>
          <h1 class="title-about-me text-3xl my-6 font-semibold">Actualidad</h1>
            <p>
                A dia de hoy estoy trabajando con Firebase en el Backend de una pagina de cursos de criptomonedas, continuo estudiando y  buscando una posicion como desarrollador web junior en donde pueda ser parte de un equipo de trabajo. En el cual pueda seguir teniendo un crecimiento en lo personal y profesional.
            </p>
       </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            dateInSpanish: timeago.format('2021-04-16', 'es_ES'),
            dateInEnglish: timeago.format('2021-04-16', 'en_US')

        }
    },
    props:{
        isInEnglish:Boolean
    },
  

}
import * as timeago from 'timeago.js';
const localeFunc = (number, index, total_sec) => {
  // number: the timeago / timein number;
  // index: the index of array below;
  // total_sec: total seconds between date to be formatted and today's date;
    return [
    ['justo ahora', 'en un rato'],
    ['hace %s segundos', 'en %s segundos'],
    ['hace 1 minuto', 'en 1 minuto'],
    ['hace %s minutos', 'en %s minutos'],
    ['hace 1 hora', 'en 1 hora'],
    ['hace %s horas', 'en %s horas'],
    ['hace 1 día', 'en 1 día'],
    ['hace %s días', 'en %s días'],
    ['hace 1 semana', 'en 1 semana'],
    ['hace %s semanas', 'en %s semanas'],
    ['hace 1 mes', 'en 1 mes'],
    [' %s meses', 'en %s meses'],
    ['hace 1 año', 'en 1 año'],
    ['hace %s años', 'en %s años'],
  ][index];
};
timeago.register('es_ES', localeFunc);

</script>
<style >
    @import url('https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,400;0,700;1,400;1,700&family=Open+Sans:ital,wght@0,600;0,700;1,500;1,600&display=swap');
   
    .title-about-me {
        font-family: 'Quicksand', sans-serif;
    }
    .about-me-element p {
        font-family: 'Merriweather', serif;    
    color: rgba(0, 0, 0, 0.699);
    font-size: 16px;
    line-height: 1.6;
    }
    .container-in-desktop {
        width: 35%;
    }
</style>