<template>
  <v-app>
    <v-content class="pa-0">
      <Outline />
      <ZevedFooter />
    </v-content>
  </v-app>
</template>

<script>
import Outline from "../components/Outline";
import ZevedFooter from "../components/ZevedFooter";

export default {
  name: "App",
  components: {
    Outline,
    ZevedFooter
  },
  data: () => ({
    //
  })
};
</script>

<style>
</style>