<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-list>
          <v-list-item-title class="pa-4 ma-0 title">
            <span class="part1-text">Zev</span><span class="part2-text">book</span>
          </v-list-item-title>

          <v-divider vertical></v-divider>

        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>mdi-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>mdi-book-open-page-variant</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Browse</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item @click="">
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        
        <v-divider vertical></v-divider>

        <v-list-item @click="">
          <v-list-item-content>
            <v-list-item-title>About Us</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      color="indigo darken-4"
      dark
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>
        <span id="part1-text">Zev</span><span id="part2-text">book</span>
      </v-toolbar-title>

      <div class="flex-grow-1"></div>
      <v-btn icon>
        <v-icon>mdi-view-dashboard</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content class="pa-0">
      <v-container class="fill-height" fluid>
        <AlgebraContent />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import AlgebraContent from "./AlgebraContent";

export default {
  components: {
    AlgebraContent
  },
  props: {
    source: String,
  },
  data: () => ({
    drawer: null,
  }),
}
</script>

<style scoped>
.part1-text {
  color: #58C4E0;
}

.part2-text {
  color: #9A72AE;
}

</style>