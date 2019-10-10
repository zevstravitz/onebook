<template>
  <v-app>
    <v-content>
      <Algebra />
    </v-content>
  </v-app>
</template>

<script>
import Algebra from "./views/Algebra";

export default {
  name: "App",
  components: {
    Algebra
  },
  data: () => ({
    //
  })
};
</script>
