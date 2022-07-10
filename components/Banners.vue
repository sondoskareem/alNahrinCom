<template>
  <v-sheet
    class="mx-auto"
    max-width="100%"
  >
    <v-slide-group
      multiple
      show-arrows
    >
      <v-slide-item
        v-for="item in items"
        :key="item"
      >
        <v-card   max-width="600"  outlined>
            <v-img
              class="white--text align-end"
              height="300px"
              :src="item.src"
            >
              <v-card-title>{{item.title}}</v-card-title>
            </v-img>

            <v-card-subtitle class="pb-0"> {{item.subtitle}}</v-card-subtitle>

            <v-card-text class="text--primary">
              <div>{{item.description}}</div>

            </v-card-text>

            <v-card-actions>
              <v-btn color="primary" text> View more ... </v-btn>
            </v-card-actions>
          </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</template>

<script>
export default {
  data: () => ({
    model: 0,
     items: [
      {
        id: 1,
        title: "Top western road trips",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img10.jpg")
      },
      {
        id: 2,
        title: "Christmas tales to read",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img11.jpg")
      },
      {
        id: 3,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img12.jpg")
      }
      ,
      {
        id: 4,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img2.jpg")
       },
       {
        id: 5,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img3.jpg")
       },
       {
        id: 6,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam albucius mei ei, debitis torquatos et pro, eos natum scribentur no. Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img4.jpg")
       },
       {
        id: 7,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img5.jpg")
       },
       {
        id: 8,
        title: "20 movies not to miss in 2020 ",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img6.jpg")
       },
       {
        id: 9,
        title: "20 movies not to miss in 2020",
        subtitle: "3,000 miles of wonder  when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        description: "Aliquam lore  Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
        src: require("../assets/images/img7.jpg")
      }
    ]
  }),
};
</script>

<style lang="scss" scoped>
</style>
