<template>
 <v-app >
    <Header />
    <Banners />
    <Popular/>
    <BestSeller/>
    <Features />
    <Organizer/>
    <Footer/>
 </v-app >
</template>

<script>
import Header from "../components/Header.vue";
import Banners from "../components/Banners.vue";
import Features from "../components/Features.vue";
import Popular from "../components/PopularEvent.vue";
import BestSeller from "../components/BestSeller.vue";
import Organizer from "../components/Organizer.vue";
import Footer from "../components/footer.vue";

export default {
  name: "Index",
  components: { Header, Banners, Features, Popular, BestSeller, Organizer, Footer },
};
</script>

<style>
</style>
