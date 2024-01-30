<template>
  <div class="work-experience-container">
    <h1 class="work-experience-title">Experiencia laboral</h1>
  </div>
</template>

<script setup>
import gsap from 'gsap';
import { ref, onMounted } from 'vue';

const titleTextAnimation = () => {
  gsap.from('.work-experience-title', {
    opacity: 0,
    y: 30,
    duration: 1,
    delay: 0.5,
    stagger: 0.2,
    scrollTrigger: {
      trigger: '.work-experience-title',
      start: 'top 100%',
      end: 'bottom 20%',
      toggleActions: 'restart none none reverse'
    }
  });
};

onMounted(() => {
  titleTextAnimation();
});
</script>

<style lang="scss" scoped>
.work-experience-container {
  background: url('/src/assets/svg/background-profile.svg') no-repeat center center fixed;
  justify-content: center;
  display: flex;
  align-items: center;
  width: 40%;
  height: auto;
  margin: 25px auto;
  padding: 0;
  border-radius: 10px;
  .work-experience-title {
    padding: 25px;
    background-color: #272c56;
    mix-blend-mode: screen;
    margin: 30px;
    border-radius: 10px;
  }
}
</style>