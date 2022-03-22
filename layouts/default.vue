<template>
  <v-app>
    <navbar />
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from '../components/partials/Navbar.vue';
export default {
  components: { Navbar },};
</script>
