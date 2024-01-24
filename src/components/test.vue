<template>
  <div class="timeline-container" align="start" ref="main">
      <v-card class="box" style="opacity: 0; transform: translateY(50px);">
        <v-card-title class="text-h6">
          TAAG GENETICS S.A. DE C.V.
        </v-card-title>
        <v-card-text class="bg-white text--primary">
          <ul>
            <li>Diseño web responsive - Vuetify framework</li>
            <li>Validación de datos de entrada - Vee-Validate</li>
            <li>Manejo de alertas (sweetalert)</li>
            <li>Consumo de API’s (AXIOS - AJAX)</li>
            <li>Diseño de mockups (Figma)</li>
            <li>Uso de metodología SCRUM</li>
            <li>Github</li>
            <li>Jira</li>
            <li>Prueba de API’s (Postman)</li>
            <li>Manejo de contenedo</li>
          </ul>
        </v-card-text>
      </v-card>
      <v-card class="box mt-3" style="opacity: 0; transform: translateY(50px);">
        <v-card-title class="text-h6">
          TDM INTERNACIONAL S.A. DE C.V.
        </v-card-title>
        <v-card-text class="bg-white text--primary">
          <ul>
            <li>Diseño web responsive - Bootstrap, VueBootstrap frameworks</li>
            <li>Validación de datos de entrada - Vuelidate</li>
            <li>Consumo de API's - Axios</li>
            <li>Control de versiones bitbucket - Flujo de trabajo trunk-based</li>
            <li>Marco de trabajo Scrum</li>
            <li>Patrón de diseño MVC</li>
            <li>Uso de arquitectura clean architecture</li>
            <li>Creación de servicios - Nodejs, express</li>
            <li>Manejo de datos - node-postgress</li>
            <li>Prueba de API's – Postman</li>
          </ul>
        </v-card-text>
      </v-card>
      <v-card class="box mt-3" style="opacity: 0; transform: translateY(50px);">
        <v-card-title class="text-h6">
          EXOS TECHNOLOGY S.A. DE C.V.
        </v-card-title>
        <v-card-text class="bg-white text--primary">
          <ul>
            <li>Diseño web responsive - Quasar framework</li>
            <li>Validación de datos de entrada - Vuelidate</li>
            <li>Consumo de API's - Axios</li>
            <li>Uso de métodos Vuex</li>
            <li>Control de versiones github</li>
            <li>Marco de trabajo Scrum</li>
            <li>Patrón de diseño MVC</li>
          </ul>
        </v-card-text>
      </v-card>
  </div>
</template>

<script setup>
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import { onMounted, ref } from 'vue';

gsap.registerPlugin(ScrollTrigger);

const items = ref([
  {
    color: '#272c56',
    icon: 'mdi-star',
    title: 'TAAG GENETICS S.A. DE C.V.',
  },
  {
    color: '#060607',
    icon: 'mdi-book-variant',
    title: 'TDM INTERNACIONAL S.A. DE C.V.',
  },
  {
    color: '#272c56',
    icon: 'mdi-airballoon',
    title: 'EXOS TECHNOLOGY S.A. DE C.V.',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
]);

onMounted(() => {
  const cards = document.querySelectorAll('.box');
  console.log(cards);
  cards.forEach((card, index) => {
    gsap.to(card, {
      opacity: 1,
      y: 30,
      scrollTrigger: {
        trigger: card,
        start: 'top 90%', // Adjust as needed
        end: 'top 60%', // Adjust as needed
        scrub: true,
      },
    });
  });
});
</script>

<style lang="scss" scoped>
.timeline-container {
  background-color: #272c56;
  justify-content: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
}
</style>
