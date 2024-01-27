<template>
  <v-parallax class="parallax" src="/src/assets/svg/background-profile.svg">
    <div class="parallax-container">
      <div class="profile-container" style="opacity: 0;">
        <v-avatar class="profile-img" image="/src/assets/img/yo.jpg"></v-avatar>
      </div>
      <div class="info-container">
        <h3 style="opacity: 0; transform: translateY(-20px)">Carlos Eduardo Arce de la Torre</h3>
        <hr style="transform-origin: left; transform: scaleX(0)">
        <h4 style="opacity: 0; transform: translateY(-20px)">Desarrollador web Frontend</h4>
      </div>
    </div>
  </v-parallax>
</template>

<script setup>
import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import { ref, onMounted } from 'vue';

gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  // Animate the profile image
  gsap.to('.profile-container', {
    opacity: 1,
    duration: 3,
    delay: 0.5,
  });

  // Animate the name
  gsap.to('.info-container h3', {
    opacity: 1,
    y: 0,
    duration: 1.5,
    delay: 0.5,
  });

  // Animate the horizontal line
  gsap.to('.info-container hr', {
    scaleX: 1,
    duration: 0.8,
    delay: 1,
  });

  // Animate the job title
  gsap.to('.info-container h4', {
    opacity: 1,
    y: 0,
    duration: 1,
    delay: 1.5,
  });
});
</script>

<style lang="scss" scoped>
.parallax {
  height: 100vh;
}
.parallax-container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #959595;
  font-size: 3rem;
  font-weight: bold;

  @media (max-width: 1790px) and (min-width: 768px) {
    flex-direction: row;
  }

  @media (max-width: 768px) {
    flex-direction: column;
  }

  .profile-container {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background-color: #272c56;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 10rem;

    @media (max-width: 1790px) and (min-width: 768px) {
      margin: 2rem;
      width: 250px;
      height: 250px;
    }

    .profile-img {
      width: 95%;
      height: 95%;
      border-radius: 50%;
    }
  }

  .info-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    @media (max-width: 1790px) and (min-width: 768px) {
        margin: 3rem;
    }

    h3 {
      font-size: 3rem;
      font-weight: bold;
      margin: 0;
      @media (max-width: 1790px) and (min-width: 768px) {
        font-size: 2rem;
      }
    }

    h4 {
      font-size: 2rem;
      font-weight: bold;
      margin: 0;
      @media (max-width: 1790px) and (min-width: 768px) {
        font-size: 1.5rem;
      }
    }
    hr {
      width: 90%;
      border: 1px solid #959595;
    }
  }
}
</style>
