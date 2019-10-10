<template>
  <v-container>
    <v-footer color="deep-purple lighten-2" padless>
        <v-row justify="center" no-gutters>
          <v-btn v-for="link in links" :key="link" color="white" text rounded class="my-2">
            {{ link }}
          </v-btn>
          <v-col class="deep-purple lighten-1 py-4 text-center white--text" cols="12">
            {{ new Date().getFullYear() }} — <strong>Zeved</strong>
          </v-col>
        </v-row>
    </v-footer>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      links: [
        'Home',
        'About Us',
        'Team',
        'Services',
        'Blog',
        'Contact Us',
      ],
    }),
  }
</script>

<style scoped>

</style>