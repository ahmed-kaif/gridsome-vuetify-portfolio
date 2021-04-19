<template>
  <v-app class="grey lighten-4">
    <TheNavbar />
    <!-- <header class="header">
      <strong>
        <g-link class="nav__link" to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header> -->

    <v-content>
      <!-- Provides the application the proper gutter -->

      <slot />
      <!-- If using vue-router -->
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import TheNavbar from '@/components/TheNavbar'

export default {
  data: () => ({
    fluid: true,
    icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
  }),
  components: {
    TheNavbar,
  },
}
</script>
<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
  text-decoration: none;
}
</style>
