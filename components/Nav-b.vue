<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      class="app-bar accent v-app-bar--fixed"
      elevate-on-scroll
      scroll-target="#scrolling-techniques-2"
      dense
      prominent

    >
      <v-app-bar-title class="text-subtitle-1 py-6 " >
        <a href="/" class="text-decoration-none">
          <strong class="white--text"><span class="color1 px-2">CSS </span> GENERATOR</strong>

        </a>
      </v-app-bar-title>
      <v-tabs align-with-title class=" hidden-xs-only " text >
        <v-spacer />
        <v-tab><a class="color2 text-capitalize text-title font-weight-regular  white--text text-decoration-none" href="/">Selektory CSS</a></v-tab>
        <v-tab>
          <nuxt-link class="color2 text-capitalize font-weight-regular  white--text text-decoration-none" to="/">
            Właściwości CSS
          </nuxt-link>
        </v-tab>
        <v-tab>
          <nuxt-link class="color2 text-capitalize font-weight-regular  white--text text-decoration-none" to="/">
            Blog
          </nuxt-link>
        </v-tab>
      </v-tabs>
      <v-spacer />
      <div class="hidden-md-and-up">
        <v-row >
          <v-dialog
            v-model="dialog"
            scrollable
            max-width="100%"
            class="align-stretch mx-0 my-0"

          >
            <template v-slot:activator="{ on, attrs }">
          <v-app-bar-nav-icon
            class="py-12"
            v-bind="attrs"
            v-on="on"
          />
            </template>
            <v-card
              class="mx-0"
              tile
            >
            <v-list
              class="mt-8 mb-8"
            >
              <template v-for="(item) in items">
                <v-list-item
                  :key="item.to"
                  exact-path
                  :to="item.to"
                  dense
                >
                  <v-list-item-content class="my-0 py-0">
                    <v-list-item-title>
                      {{ item.title }}
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </template>
            </v-list>
            </v-card>
          </v-dialog>
        </v-row>
      </div>
    </v-app-bar>
    <v-sheet
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 90px;" />
    </v-sheet>
  </v-card>
</template>

<script>
export default {
  name: 'NavB',
  data: () => ({
    drawer: false,
    group: null,
    dialog: false,
    items: [
      { title: 'Generatory', to: '/' },
      { title: 'Selektory CSS', to: '/' },
      { title: 'Właściwości CSS', to: '/' },
      { title: 'Blog', to: '/' }
    ]
  })
}
</script>

<style scoped>
.color1{
  color: #5983fc;
}
.color2{
  color: white;
}
.color2:hover{
  color: #5983fc;
}
</style>
