<template>
  <div class="cards-container">
    <v-card v-for="(skill, index) in skills"
      :key="skill"
      title="Card title" 
      subtitle="Subtitle" 
      text="Prueba de texto"
      elevation="16"
      class="custom-card"
      :data-index="index"
    ></v-card>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
import gsap from 'gsap';

// Variables
const skills = [
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
  }
];

// Animations
const skillsAnimation = () => {
  gsap.from('.custom-card', {
    y: 300,
    duration: 0.8,
    delay: 0.2,
    stagger: 0.2,
    opacity: 0,
    scrollTrigger: {
      trigger: '.custom-card',
      start: 'top 120%',
      end: 'bottom 20%',
      toggleActions: 'restart none none reverse'
    }
  });
}

// On mounted
onMounted(() => {
  skillsAnimation();
});
</script>

<style lang="scss" scoped>
.cards-container {
  margin: 5rem 5rem 0 5rem;
  display: flex;
  justify-content: space-around; 
  flex-wrap: wrap;
  .custom-card {
    width: 200px;
    margin: 16px;
  }
}

</style>