<template>
    <v-row>
      <v-col cols="12">
        <v-card class="accent">
        <v-card-text >
          <strong class=" text-h4  white--text">Box Shadow Generator</strong>
          <p
            class="text-h6 text-start secondary--text font-weight-light"
          >
            Wygodne narzędzie, dzięki któremu wygenerujesz gotowe reguły CSS. Dostosuj box shadow i skopiuj gotowy kod.
          </p>
        </v-card-text>
        </v-card>
      </v-col>
      <BoxShadow />
    </v-row>
</template>

<script>
import BoxShadow from "../components/BoxShadow";
export default {
  name: 'InspirePage',
  components: {BoxShadow}
}
</script>
