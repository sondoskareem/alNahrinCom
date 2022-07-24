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
      <div class="more-details">
        <div class="details-top">
          <div class="details-time">
            <p>
              <v-icon medium color="primary">mdi-clock</v-icon> Start :
              01/01/2022 00:00:00
            </p>
            <p>
              <v-icon medium color="primary">mdi-clock</v-icon> End : 01/01/2022
              00:00:00
            </p>
          </div>

          <div class="detail-action">
            <v-btn>Add to calender</v-btn>
            <v-btn>Remide me</v-btn>
          </div>
        </div>

        <div class="details-bottom">

          <div class="share-socials">
           <p class="share-event-p">Share the event with your friends</p>
            <a> <v-icon medium color="black">mdi-skype</v-icon> </a>
            <a><v-icon medium color="black">mdi-instagram</v-icon></a>
            <a><v-icon medium color="black">mdi-facebook</v-icon></a>
          </div>

          <p>
            Or by invitation link
            <a><v-icon medium color="black">mdi-link</v-icon></a>
          </p>
        </div>
      </div>

      <div class="details">
        <template>
          <v-simple-table class="rtl-table">
            <template v-slot:default>
              <thead>
                <tr>
                  <th class="text-right">Details</th>
                  <th class="text-right">Reg. Deadline</th>
                  <th class="text-right">Price</th>
                  <th class="text-right">Number</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="item in pricing" :key="item.name">
                  <td>{{ item.name }}</td>
                  <td>{{ item.deadline }}</td>
                  <td>{{ item.price }}</td>
                  <td>
                    <input v-model="item.number" type="number" />
                    <!-- {{ item.number }} -->
                  </td>
                </tr>
              </tbody>
              <v-flex class="table-btn">
                <v-btn>Save</v-btn>
                <v-btn>Cancele</v-btn>
              </v-flex>
            </template>
          </v-simple-table>
        </template>
      </div>
    </div>
  </div>
</template>

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
    editedItem: {
      number: 0,
    },
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
        number: 0,
      },
      {
        name: "Normal ticket",
        price: 237,
        deadline: "2022/10/6",
        number: 0,
      },
      {
        name: "late",
        price: 262,
        deadline: "2022/10/2",
        number: 0,
      },
      {
        name: "Programming workshop",
        price: 305,
        deadline: "2022/10/4",
        number: 0,
      },
      {
        name: "Cryptocurrency training workshop",
        price: 356,
        deadline: "2022/10/8",
        number: 0,
      },
      {
        name: "Legal challenges training workshop",
        price: 375,
        deadline: "2022/10/11",
        number: 0,
      },
    ],
  }),

  methods: {
    onButtonClick(item) {
      console.log("click on " + item.number);
      this.editedIndex = this.desserts.indexOf(item);
      this.editedItem = Object.assign({}, item);
      this.dialog = true;
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
  padding: 0 3rem;

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
  background-size: cover;
}
.rtl-table , .more-details {
  direction: rtl;
  text-align: right;
}

.table-btn {
  margin-top: 1.5rem;
}
.details {
  flex-grow: 1;
  width: 60%;
}
.more-details {
  /* background-color: rgb(113, 144, 171); */
  height: 100%;
  width: 40%;
  display: flex;
  flex-direction: column;
  gap: 3rem;
  padding: 2rem ;


}
.details-top{
}
.details-time {
  font-size: 0.9rem;
}

.details-time,
.detail-action , .share-socials {
  display: flex;
  /* flex-direction:column; */
  gap: 2rem;
}
.detail-action > * {
  font-size: 0.8rem;
}
.details-bottom {
  display: flex;
  flex-direction: column;
  gap: .7rem;
  justify-items: center;
}
.share-event-p{
  margin-bottom: .3rem;
}
</style>
