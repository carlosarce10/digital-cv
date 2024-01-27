<template>
  <div class="work-experience-container">
    <h1 class="work-experience-title">Experiencia laboral</h1>
  </div>
  <div ref="cardContainer" class="cards-container">
    <div v-for="(card, index) in cards" :key="index" class="card-wrapper">
      <div class="card-contents">
        <div class="card-description">
          <h1>{{ card.title }}</h1>
          <p>{{ card.subtitle }}</p>
          <ul class="card-experience">
            <li v-for="(item, index) in card.descrpiton" :key="index">{{ item.text }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <div class="spacer"></div>
  
</template>

<script>
import { ref, onMounted } from 'vue';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';

export default {
  setup() {
    const cardContainer = ref(null);
    // Variables
    const cards = [
      {
        title: 'TAAG GENETICS S.A. DE C.V.',
        subtitle: 'Coyoacán Méx. nov. 2022-actualidad',
        descrpiton: [
          {
            text: 'Diseño web responsive'
          },
          {
            text: 'Validación de datos de entrada'
          },
          {
            text: 'Consumo de API\'s'
          },
          {
            text: 'Uso de métodos Vuex'
          },
          {
            text: 'Control de versiones github'
          },
          {
            text: 'Marco de trabajo Scrum'
          },
          {
            text: 'Patrón de diseño MVC'
          },
        ]
      },
      {
        title: 'TDM INTERNACIONAL S.A. DE C.V.',
        subtitle: 'Cuernavaca Mor. oct. 2021 – nov. 2022',
        descrpiton: [
          {
            text: 'Diseño web responsive'
          },
          {
            text: 'Validación de datos de entrada'
          },
          {
            text: 'Consumo de API\'s'
          },
          {
            text: 'Uso de métodos Vuex'
          },
          {
            text: 'Control de versiones github'
          },
          {
            text: 'Marco de trabajo Scrum'
          },
          {
            text: 'Patrón de diseño MVC'
          },
        ]
      },
      {
        title: 'EXOS TECHNOLOGY S.A DE C.V',
        subtitle: 'Cuernavaca Mor.ago. 2020 - ene. 2021',
        descrpiton: [
          {
            text: 'Diseño web responsive'
          },
          {
            text: 'Validación de datos de entrada'
          },
          {
            text: 'Consumo de API\'s'
          },
          {
            text: 'Uso de métodos Vuex'
          },
          {
            text: 'Control de versiones github'
          },
          {
            text: 'Marco de trabajo Scrum'
          },
          {
            text: 'Patrón de diseño MVC'
          },
        ]
      },
    ];

    // Animations
    const cardsAnimation = () => {
      cards.value = Array.from(cardContainer.value.querySelectorAll('.card-wrapper'));

      let stickDistance = 350;
      let firstCardST = ScrollTrigger.create({
        trigger: cards.value[0],
        start: 'center center'
      });
      let lastCardST = ScrollTrigger.create({
        trigger: cards.value[cards.value.length - 1],
        start: 'start start',
        endTrigger: cardContainer.value,
        end: 'bottom bottom',
        pin: true,
        pinSpacing: true, // Cambiado a true
        ease: 'none',
        toggleActions: 'restart none none reverse'
      });

      cards.value.forEach((card, index) => {
        var scale = 1 - (cards.value.length) * 0.025;
        let scaleDown = gsap.to(card, {
          scale: scale,
          transformOrigin: '50% ' + (lastCardST.start)
        });

        ScrollTrigger.create({
          trigger: card,
          start: 'center center',
          end: () => lastCardST.start + stickDistance,
          pin: true,
          pinSpacing: false,
          ease: 'none',
          animation: scaleDown,
          toggleActions: 'restart none none reverse'
        });
      });
    };
    const textAnimation = () => {
      gsap.from('.card-description', {
        opacity: 0,
        y: 30,
        duration: 1,
        delay: 0.5,
        stagger: 0.2,
        scrollTrigger: {
          trigger: '.card-description',
          start: 'top 100%',
          end: 'bottom 20%',
          toggleActions: 'restart none none reverse'
        }
      });
    };

      
    onMounted(() => {
      cardsAnimation();
      textAnimation();
    });

    return {
      cardContainer,
      cards,
    };
  },
};
</script>

<style lang="scss" scoped>
.cards-container {
  background: url('/src/assets/svg/background-profile.svg') no-repeat center center fixed;
  justify-content: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 40%;
  height: auto;
  margin: 25px auto;
  padding: 0;
  border-radius: 10px;
  .card-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
  }
  
  .card-contents {
    width: 500px;
    height: auto;
    background-color: #272c56c5;
    border-radius: 10px;
    padding-bottom: 20px;
    .card-experience {
      margin: 30px 0px 0px 40px ;
      li {
        margin: 0;
        padding: 0;
        font-size: 14px;
        font-weight: 400;
      }
    }
  }
}

img {
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  opacity: 0.8;
  object-fit: cover;
}

.card-description {
  color: rgba(255, 255, 255, 0.808);

  h1,
  p {
    margin: 0;
    text-align: left;
    margin-left: 20px;
  }
  h1 {
    font-size: 28px;
    font-weight: 700;
  }
  p {
    font-size: 14px;
    font-weight: 400;
  }
}
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
/* .work-experience-title {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 50px;
  color: #272c56;
  background-color: #000;
  padding: 10px 20px;
  border:#000 1px solid;
  border-radius: 10px;
  justify-content: center;
  display: flex;
  margin: 15px;
} */
</style>