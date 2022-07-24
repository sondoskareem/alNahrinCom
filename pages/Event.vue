<template>
  <!-- <v-container> -->
  <!-- <v-row> -->
  <div>
    <v-row class="container1">
      <div class="card-container">
        <v-flex class="card-flex">
          <div class="card-text">
            <h4>{{ item.title }}</h4>

            <p>
              <v-icon medium color="primary"> mdi-clock </v-icon>
              {{ item.time }}
            </p>
            <p>
              <v-icon medium color="primary"> mdi-map-marker </v-icon>Baghdad
              Outer karada 14st
            </p>

            <h6>
              <b>{{ item.subtitle }}</b>
            </h6>
            <p>{{ item.description }}</p>
            <v-flex>
              <v-btn
                class="ma-2"
                :loading="loading"
                :disabled="loading"
                color="primary"
                @click="loader = 'loading'"
              >
                Contact Us
              </v-btn>
              <v-btn
                class="ma-2"
                :loading="loading"
                :disabled="loading"
                color="secondary"
                @click="loader = 'loading'"
              >
                Follow
              </v-btn>
            </v-flex>

            <!-- <p>Any1</p> -->
          </div>
          <div class="card-img">
            <!-- <v-img :src="item.src" height="100%"></v-img> -->
            <!-- <p>Any</p> -->
          </div>
        </v-flex>
      </div>
    </v-row>

    <div class="container2">
      <div class="more-details"></div>

      <div class="details">
        <v-data-table :headers="headers" :items="pricing" class="elevation-1">
          <template v-slot:top>
            <v-dialog v-model="dialog" persistent max-width="290">
              <v-card>
                <v-card-title class="text-h5">
                  Number of tickets?
                </v-card-title>
                <v-col cols="12" sm="6" md="4">
                  <v-select
                    :items="['1', '2', '3', '4']"
                    label="Number*"
                    required
                  ></v-select>
                  <v-spacer></v-spacer>
                </v-col>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn color="primary darken-1" text @click="dialog = false">
                    Cancele
                  </v-btn>
                  <v-btn color="primary darken-1" text @click="dialog = false">
                    Save
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </template>

          <template v-slot:item.number="{ item }">
            <v-icon color="black" @click="dialog = true">mdi-plus</v-icon>
          </template>
        </v-data-table>
      </div>
    </div>
  </div>

  <!-- </v-row> -->
  <!-- </v-container> -->
</template>

<script>
export default {
  data: () => ({
    model: 0,
    show: false,
    dialog: false,
    item: {
      id: 1,
      title: "Top western road trips",
      subtitle: " scrambled it to make a type specimen book.",
      description:
        "specimen book. It ucius mei ei, debitis torquatos et pro, eos natum scribentur no. Putant verear constituto te qui. Adolescens persequeris vim ei. It ucius mei ei, debitis torquatos et pro, eos natum scribentur no. Putant verear constituto te qui. Adolescens persequeris vim ei. Vel nullam reprimique te.",
      src: require("../assets/images/img3.jpg"),
      time: "2022/9/9 15:30",
    },
    headers: [
      {
        text: "Details",
        align: "start",
        value: "name",
      },
      { text: "Reg. Deadline", value: "deadline" },
      { text: "Price", value: "price" },
      { text: "Number", value: "number" },
    ],
    pricing: [
      {
        name: "Early bird tickets",
        deadline: "2022/10/10",
        price: 159,
        number: 24,
      },
      {
        name: "Normal ticket",
        price: 237,
        deadline: "2022/10/6",
        number: 37,
      },
      {
        name: "late",
        price: 262,
        deadline: "2022/10/2",
        number: 23,
      },
      {
        name: "Programming workshop",
        price: 305,
        deadline: "2022/10/4",
        number: 67,
      },
      {
        name: "Cryptocurrency training workshop",
        price: 356,
        deadline: "2022/10/8",
        number: 49,
      },
      {
        name: "Legal challenges training workshop",
        price: 375,
        deadline: "2022/10/11",
        number: 94,
      },
    ],
  }),

  methods: {
    onButtonClick(item) {
      console.log("click on " + item.number);
      this.dialog = true;
    },
  },
};
</script>

<style lang="css" scoped>
@media only screen and (min-width: 1200px) {
  .container1 {
    height: 70vh;
  }
}
.container1 {
  width: 100%;
  max-width: 100vw;
  background-color: rgb(255, 255, 255);
  position: relative;
}
.container2 {
  height: 60vh;
  width: 100%;
  max-width: 100vw;
  margin: 10rem 0;
  display: flex;
  padding: 3rem;

  justify-content: center;
  /* margin-top: 10rem; */
}
.card-container {
  position: absolute;
  height: fit-content;
  width: 90%;
  left: 50%;
  top: 10%;
  transform: translateX(-50%);
  /* background-color: rgb(243, 243, 243); */
}
.card-flex {
  display: flex;

  flex-direction: row;
}

.card-text {
  flex-basis: fill;
  padding: 3rem;
  display: flex;
  gap: 10px;
  flex-direction: column;
    background-color: rgb(243, 243, 243);

  /* width: 70%; */
}
.bodd {
  font-weight: bold;
}
.card-img {
  overflow: hidden;
  width: 60%;
  /* height: 100%; */
  background-image: url("../assets/images/img3.jpg");
  background-size:cover;
}
.details {
  flex-grow: 1;
  width: 60%;
}
.more-details {
  background-color: rgb(113, 144, 171);
  height: 100%;
  width: 30%;
}
</style>
