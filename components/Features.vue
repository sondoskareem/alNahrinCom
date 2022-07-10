<template>
  <v-container fluid class="mx-auto" max-width="100%" mb-13>
     <h2 class="text-center" style="margin-bottom: 52px !important">
     OUR SERVICES FOR THE ORGANIZERS
    </h2>
    <v-sheet class="mx-auto" max-width="100%">
      <v-slide-group multiple show-arrows>
        <v-slide-item v-for="item in items" :key="item">
          <v-card class="mx-auto" max-width="344" outlined>
            <v-list-item three-line>
              <v-list-item-content>
                <div class="text-overline mb-4">OVERLINE</div>
                <v-list-item-title class="text-h5 mb-1">
                  {{item.title}}
                </v-list-item-title>
                <v-list-item-subtitle>
                 {{item.subtitle}}
                  </v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-card-actions>
              <v-btn color="primary" outlined rounded text> VISIT </v-btn>
            </v-card-actions>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    model: 0,
    items: [
      {
        id: 1,
        title: "Marketing Tool",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img10.jpg"),
      },
      {
        id: 2,
        title: "Social Media",
        subtitle:" scrambled it to make a type specimen book.",

        src: require("../assets/images/img11.jpg"),
      },
      {
        id: 3,
        title: "Google Ads",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img7.jpg"),
      },
      {
        id: 4,
        title: "Make Trend",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img2.jpg"),
      },
      {
        id: 5,
        title: "Customer Engagment",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img3.jpg"),
      },
      {
        id: 6,
        title: "Posts and stories",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img14.jpg"),
      },
      {
        id: 7,
        title: "Keeo Your Self Updated",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img12.jpg"),
      },
      {
        id: 8,
        title: "Increase Your Income",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img13.jpg"),
      },
      {
        id: 9,
        title: "Create Didate Events",
        subtitle:" scrambled it to make a type specimen book.",
        src: require("../assets/images/img10.jpg"),
      },
    ],
  }),
};
</script>

<style lang="css" scoped>
.container {
  height: fit-content;
}
</style>
