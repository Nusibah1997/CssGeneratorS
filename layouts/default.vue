<template>
  <v-app dark>
    <nav-b/>
    <v-main class="bg">
      <v-container class="px-0 ma-0" style="" >
        <Nuxt />
      </v-container>
    </v-main>
      <FooterP
        app
      />
  </v-app>
</template>

<script>
import NavB from "../components/Nav-b";
import FooterP from "../components/Footer-p";
export default {
  name: 'DefaultLayout',
  components: {FooterP, NavB},
  data () {
    return {
    }
  }
}
</script>

<style>
.v-application {
  font-family: 'Roboto', 'sans-serif' !important;
}
.bg{
  background-color: #1f2024;
}
</style>
