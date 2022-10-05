<template>
  <v-row class="mx-0" style="background-color: lavender ">
      <v-card  class="ma-16 pa-8 rounded-lg" max-width="1000" style=" white-space: nowrap; background-color: white">
        <v-slide-group
          multiple
          show-arrows
        >
          <v-slide-item
            v-for="card in cards"
            :key="card.title"
          >

            <v-btn
              height="50"
              width="150"
              class="borders my-2 mx-2 "
              rounded-lg
              outlined
              align="center"
              justify="center"
              v-text="card.title"
              to="/inspire"
              nuxt
            >
            </v-btn>
          </v-slide-item>
        </v-slide-group>
      </v-card>
    <options-box-shadow />
  </v-row>
</template>

<script>
import OptionsBoxShadow from "./optionsBoxShadow";
export default {
  name: "BoxShadow",
  components: {OptionsBoxShadow},
  data: () => ({
    model: null,
    cards: [
      { title: 'Box shadow' },
      { title: 'Text shadow'},
      { title: 'Flexbox' },
      { title: 'Border radius'},
      { title: 'Gradient'},
      { title: 'Transition' },
      { title: 'Transform' },
      { title: 'Background' },
      { title: 'Button'},
    ]
  }),
}
</script>

<style scoped>
.borders{
  border-width: 2px;
  color: #5983fc;
  background-color: white ;
}
.borders:hover{
  background-color: #5983fc;
  color: #ffffff;
}
</style>
