<template>
  <v-row class="mt-4 mb-8">
    <v-row>
    <v-col md="3"></v-col>
    <v-col md="7" cols="12">
        <v-card-text align="center">
          <strong class=" text-h4 white--text"><span class="color1 px-2">CSS </span> GENERATOR</strong>
          <p
            class="my-6 text-subtitle-1 text-start secondary--text font-weight-regular"
            align="center"
            justify="center"
          >
            Prosty generator, za pomocą którego dobierzesz odpowiednie wartości dla wybranych właściwości CSS.
            Wygodne dostosowanie parametrów za pomocą suwaków,
            podgląd na żywo i błyskawiczne kopiowanie gotowego kodu CSS.
          </p>
        </v-card-text>
    </v-col>
  </v-row>
  <v-row>
    <v-col md="3">
    </v-col>
    <v-col md="7" cols="6">
      <v-row dense>
        <v-col
          v-for="card in cards"
          :key="card.title"
          :cols="card.flex"
          class="mx-0"
          md="4"
          sm="6"
          >
          <v-btn
            height="60"
            width="190"
            class="borders my-2 "
            rounded-lg
            outlined
            align="center"
            justify="center"
            v-text="card.title"
            to="/inspire"
            nuxt
          >
          </v-btn>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data: () => ({
    cards: [
      { title: 'Box shadow',  flex: 12 },
      { title: 'Text shadow',  flex: 12 },
      { title: 'Flexbox',  flex: 12 },
      { title: 'Border radius',  flex: 12 },
      { title: 'Gradient',  flex: 12 },
      { title: 'Transition',  flex: 12 },
      { title: 'Transform',  flex: 12 },
      { title: 'Background',  flex: 12 },
      { title: 'Button',  flex: 12 },
    ]
  })
}
</script>

<style scoped>
.color1{
  color: #5983fc;
}
.borders{
  border-width: 2px;
  color: #5983fc;
}
.borders:hover{
  background-color: #5983fc;
  color: #1f2024;
}
</style>

