<template>
    <h1 class="text-center title">Experiencia laboral</h1>
  <v-timeline class="mx-5 timeline-container">
    <v-timeline-item
      :dot-color="'#272c56'"
      fill-dot
    >
      <v-card>
        <v-card-title class="bg-purple-lighten-2">
          <v-icon
            size="large"
            class="me-4"
            icon="mdi-magnify"
          ></v-icon>
          <h2 class="font-weight-light">
            TAAG GENETICS S.A. DE C.V.
          </h2>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
        </v-card-text>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      :dot-color="'#060607'"
      fill-dot
      size="x-small"
    >
      <v-card>
        <v-card-title class="bg-amber-lighten-1 justify-end">
          <h2 class="me-4 font-weight-light">
            Title 2
          </h2>
          <v-icon
            size="large"
            icon="mdi-home-outline"
          ></v-icon>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
        </v-card-text>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      dot-color="cyan-lighten-1"
      fill-dot
    >
      <v-card>
        <v-card-title class="bg-cyan-lighten-1">
          <v-icon
            class="me-4"
            size="large"
            icon="mdi-email-outline"
          ></v-icon>
          <h2 class="font-weight-light">
            Title 3
          </h2>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
        </v-card-text>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      dot-color="red-lighten-1"
      fill-dot
      size="x-small"
    >
      <v-card>
        <v-card-title class="bg-red-lighten-1 justify-end">
          <h2 class="me-4 font-weight-light">
            Title 4
          </h2>
          <v-icon
            size="large"
            icon="mdi-account-multiple-outline"
          ></v-icon>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
        </v-card-text>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      dot-color="green-lighten-1"
      fill-dot
    >
      <v-card>
        <v-card-title class="bg-green-lighten-1">
          <v-icon
            class="me-4"
            size="large"
            icon="mdi-phone-in-talk"
          ></v-icon>
          <h2 class="font-weight-light">
            Title 5
          </h2>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit.
        </v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>
<script>

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
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.title {
  margin: 1rem;
  color: #272c56;
}
</style>