<template>
  <div class="cards-container">
    <v-card v-for="skill in skills"
      :key="skill"
      title="Card title" 
      subtitle="Subtitle" 
      text="Prueba de texto"
      elevation="16"
      class="custom-card"
    ></v-card>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';

const skills = ref([
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
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
  {
    color: '#060607',
    icon: 'mdi-layers-triple',
  },
]);
</script>

<style lang="scss" scoped>
.cards-container {
  margin-top: 5rem;
  display: flex;
  justify-content: space-around; 
  flex-wrap: wrap;
}

.custom-card {
  width: 200px;
  margin: 16px;
}
</style>