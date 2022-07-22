<template>
  <v-app>
    <v-main>
      <Header/>
      <Nuxt />
      <AppFooter/>
    </v-main>
  </v-app>
</template>

<script>
import Header from '../components/Header.vue';
import AppFooter from '../components/AppFooter.vue';
export default { components: { Header, AppFooter } };
</script>

<style scoped>
</style>
