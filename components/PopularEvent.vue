<template>
  <v-container my-13>
    <h2 class="text-center" style="margin-bottom: 52px !important">
   THE MOST POPULAR EVENTS
    </h2>
    <v-row  class="flex-wrap">
      <v-col v-for="item in items" :key="item.id">
          <v-card class="mx-auto" max-width="344">
            <v-img
              :src="item.src"
              height="200px"
            ></v-img>
            <v-card-title> {{item.title}}</v-card-title>
            <v-card-subtitle>{{item.subtitle}}  </v-card-subtitle>
            <v-card-text style="overflow-y: auto; height:100px" > {{item.description}}
           <v-chip-group column>
              <v-chip color="primary">{{item.time}}</v-chip>
            </v-chip-group>
            </v-card-text>
            <v-card-actions>
              <v-btn color="primary" text> Explore</v-btn>
            </v-card-actions>
          </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
   name: "PopularEvent",
  data: () => ({
    model: 0,
    show: false,
    items: [
      {
        id: 1,
        title: "Top western road trips",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "specimen book.  Putant verear constituto te qui. Ado ei. Vel nullam reprimique te.",
        src: require("../assets/images/img10.jpg"),
        time:"2022/9/9 15:30"
      },
      {
        id: 2,
        title: "Christmas tales to read",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "specimen book. publishing stituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img11.jpg"),
        time:"2022/9/9 15:30"
      },
      {
        id: 3,
        title: "20 movies not to miss in 2020",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "Idebitis torquatos et pro, eos natum te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img12.jpg"),
        time:"2022/9/9 15:30"
      },
      {
        id: 4,
        title: "20 movies not to miss in 2020",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "specimen book. It has survived ebitis torquatos et pro, vei. Vel nullam reprimique te.",
        src: require("../assets/images/img2.jpg"),
        time:"2022/9/9 15:30"
      },
      {
        id: 5,
        title: "20 movies not to miss in 2020",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "specimen book. tur no. Putant verear constitut persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img3.jpg"),
        time:"2022/9/9 15:30"
      },
      {
        id: 6,
        title: "20 movies not to miss in 2020",
        subtitle:
          " scrambled it to make a type specimen book.",
        description:
          "Aliquam albucius mei ei, debitis torquatosolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img4.jpg"),
        time:"2022/9/9 15:30"
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
</style>
