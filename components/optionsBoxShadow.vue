<template>
  <v-row>
    <v-col
      cols="12"
      md="5"
    >
  <v-card class=" mx-16 rounded-lg e4" color="white" >
    <v-card-title  class="text-h5 colorText">CSS box-shadow</v-card-title>
    <v-card-text>
      <v-container fluid>
        <v-row>
          <v-col cols="12" class="py-0">
            <v-card-title class="text-subtitle-1 colorText">Horizontal</v-card-title>
            <v-slider
              v-model="red"
              :max="255"
              class=" mt-0 align-center"
            >
              <template v-slot:append>
                <v-text-field
                  v-model="red"
                  class=" my-0 py-0"
                  type="number"
                ></v-text-field>
              </template>
            </v-slider>
          </v-col>

          <v-col cols="12" class="py-0">
            <v-card-title class="py-0 my-0 text-subtitle-1 colorText">Vertical</v-card-title>
            <v-slider
              v-model="green"
              :max="255"
              class="align-center"
            >
              <template v-slot:append>
                <v-text-field
                  v-model="green"
                  class="mt-0 pt-0"
                  type="number"
                  style="width: 60px"
                ></v-text-field>
              </template>
            </v-slider>
          </v-col>

          <v-col cols="12" class="py-0">
            <v-card-title class="py-0 my-0 text-subtitle-1 colorText">Blur</v-card-title>
            <v-slider
              v-model="blue"
              :max="255"
              class="align-center"
            >
              <template v-slot:append>
                <v-text-field
                  v-model="blue"
                  class="mt-0 pt-0"
                  type="number"
                  style="width: 60px"
                ></v-text-field>
              </template>
            </v-slider>
          </v-col>
          <v-col cols="12" class="py-0">
            <v-card-title class="py-0 my-0 text-subtitle-1 colorText">Spread</v-card-title>
            <v-slider
              v-model="red"
              :max="255"
              class="align-center"
            >
              <template v-slot:append>
                <v-text-field
                  v-model="red"
                  class="mt-0 pt-0"
                  type="number"
                  style="width: 60px"
                ></v-text-field>
              </template>
            </v-slider>
          </v-col>
          <v-col cols="12" class=" py-0">
            <v-card-title class="justify-space-between text-subtitle-1 colorText">
              Kolor:
              <v-btn
                height="30"
                width="20"
                x-small
                rounded-lg
                nuxt
                v-bind="attrs"
                v-on="on"
              >
              </v-btn>
            </v-card-title>
          </v-col>
          <v-col cols="12" class=" py-0">
            <v-card-title class="justify-space-between text-subtitle-1 colorText">
              Inset:
              <v-switch
                v-model="switch1"
              ></v-switch>
            </v-card-title>
          </v-col>
        </v-row>
      </v-container>
    </v-card-text>
  </v-card>
    </v-col>
    <v-col cols="12" md="7" class="justify-center">
      <v-card class="justify-center rounded-lg py-16 mr-12" height="600" color="white">
      <v-card
        class=" rounded-lg mx-auto my-16"
        height="300"
        max-width="300"
        color="white"
        style="justify-content: center; align-items: center"
      >
      </v-card>
      </v-card>
    </v-col>

  <v-row>
    <v-col cols="12" md="5">
    </v-col>
    <v-col cols="12" md="7" class="justify-center">
      <v-card class="justify-center rounded-lg py-16 mr-12" height="250" color="white">
        <v-sheet
          dark
          class="pa-4 "
          height="150"
        >
          <pre>{{ showColor }}</pre>
        </v-sheet>
      </v-card>
    </v-col>
  </v-row>
  </v-row>
</template>

<script>
export default {
  name: "optionsBoxShadow",
  data () {
    return {
      red: 64,
      green: 128,
      blue: 0,
      rgba: { r: 255, g: 0, b: 255, a: 1 },
      picker:null
    }
  },
  computed: {
    color: {
      get () {
        return this[this.type]
      },
      set (v) {
        this[this.type] = v
      },
    },
    showColor () {
      if (typeof this.color === 'string') return this.color

      return JSON.stringify(Object.keys(this.color).reduce((color, key) => {
        color[key] = Number(this.color[key].toFixed(2))
        return color
      }, {}), null, 2)
    },
  },
}
</script>

<style scoped>
.colorText{
  color: #1f2024;
}
</style>
