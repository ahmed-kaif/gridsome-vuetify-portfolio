<template>
  <nav>
    <v-toolbar flat app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        Rownok Asif
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat color="grey">
        About
      </v-btn>
    </v-toolbar>
    <v-navigation-drawer
      v-model="drawer"
      temporary
      absolute
      bottom
      class="indigo"
    >
      <p>Test</p>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    }
  },
}
</script>

<style scoped></style>
