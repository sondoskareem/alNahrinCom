<template>
  <v-container fluid class="mx-auto" max-width="80%">
     <h2 class="text-center" >
      THE MOST POPULAR ORGANIZERS
    </h2>
    <v-row class="logo-gallery">
      <v-col v-for="item in items" :key="item" class="d-flex child-flex" cols="4" style=" overflow: hidden;" >
          <img :src="item.src" class="colored"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    show: false,
    items: [
      {
        id: 1,
        src: require("../assets/images/logo7.jpeg"),
      },
      {
        id: 2,
        src: require("../assets/images/logo2.png"),
      },
      {
        id: 3,
        src: require("../assets/images/logo5.jpeg"),
      },
      {
        id: 4,
        src: require("../assets/images/logo9.jpeg"),
      },
      {
        id: 5,
        src: require("../assets/images/logo3.jpeg"),
      },
      {
        id: 6,
        src: require("../assets/images/logo4.png"),
      },

    ],
  }),
};
</script>

<style>
.colored{
  /* height: 100px; */
  height: fit-content;
  width: 100px;
  vertical-align: middle;
}
.logo-gallery{
  padding: 12rem;
  margin-top: -10rem;
}
</style>
