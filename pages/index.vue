<template>
 <v-app >
   <Banners />
    <Popular/>
    <BestSeller/>
    <Features />
    <Organizer/>
 </v-app >
</template>

<script>
import Banners from "../components/Banners.vue";
import Features from "../components/Features.vue";
import Popular from "../components/PopularEvent.vue";
import BestSeller from "../components/BestSeller.vue";
import Organizer from "../components/Organizer.vue";

export default {
  name: "Index",
  components: {  Banners, Features, Popular, BestSeller, Organizer },
};
</script>

<style>
</style>
