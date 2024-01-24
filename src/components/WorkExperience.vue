<template>
  <v-timeline class="timeline-container" align="start">
    <v-timeline-item
      v-for="(item, i) in items"
      :key="i"
      :dot-color="item.color"
      :icon="item.icon"
      fill-dot
      class="box"
    >
      <v-card>
        <v-card-title :class="['text-h6', `${item.color}`]">
          {{ item.title }}
        </v-card-title>
        <v-card-text class="bg-white text--primary">
          <p>Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.</p>
        </v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>
<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  data: () => ({
    items: [
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
    ],
  }),
  mounted() {},
  methods: {},
}
</script>
<style lang="scss" scoped>
.timeline-container {
  background-color: rgb(242, 242, 242);
}
</style>