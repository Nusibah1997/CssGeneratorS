<template>
  <v-footer class=" accent" padless>
    <v-row class="my-md-5">
    <v-col
      class="text-sm-center secondary--text "
      md="6"
      cols="12"
    >
      © {{ new Date().getFullYear() }} — <strong>cssgenerator.pl</strong>
    </v-col>
    <v-col
      class="text-center font-weight-thin"
      md="6"
      cols="12"
    >
      <strong class="secondary--text">autor:  <a href="/" class="text-decoration-none pl-1"> <strong> Marek Foltański</strong> </a></strong>
    </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  name: "Footer-p"
}
</script>

<style scoped>

</style>
