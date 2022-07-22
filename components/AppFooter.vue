<template>
  <v-footer padless color="primary" style="padding: 3rem">
    <div class="footer-custom">
      <div class="footer-container">
        <div class="more-in-home">
          <p>MORE IN OUR COMPANY</p>

          <ul class="more-in-home-list">
            <li v-for="item in items" :key="item">
              <a>{{ item.title }}</a>
            </li>
          </ul>
        </div>

        <div class="line-horizonatl"></div>

        <div class="about-somo">
          <p>TOPICS YOU MAY LIKE</p>
          <ul class="more-in-home-list">
            <li><a href="/">How to create events</a></li>
            <li><a href="/">Become a succefull business owner </a></li>
            <li><a href="/">Start your own company </a></li>
            <li><a href="/">Lorem ipsum dolor sit amet. </a></li>
            <li><a href="/">Amet ipsum dolor sit. </a></li>
          </ul>
        </div>

        <div class="contact-us">
          <p>Contact us</p>
          <ul>
            <li>
              <a href="/">
                <v-icon large color="darken-2"> mdi-twitter</v-icon>
              </a>
            </li>
            <li>
              <a href="/">
                <v-icon large color="darken-2"> mdi-facebook </v-icon>
              </a>
            </li>
            <li>
              <a href="/">
                <v-icon large color="darken-2"> mdi-whatsapp </v-icon>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </v-footer>
</template>


<script>
export default {
  data: () => ({
    model: 0,
    show: false,
    items: [
      {
        id: 1,
        title: "Best seller for this week",
      },
      {
        id: 2,
        title: "Our servicse",
      },
      {
        id: 3,
        title: "How to make events",
      },
      {
        id: 4,
        title: "Contact us",
      },
      {
        id: 5,
        title: "Tell your story",
      },
      {
        id: 6,
        title: "Become organizer",
      },
    ],
  }),
};
</script>

<style>
.footer-custom {
  width: 100%;
  height: 20rem;
}
.footer-container {
  padding: 2rem 4rem;
  width: 100%;
  height: 100%;
  display: flex;
  gap: 100px;
  /* justify-content: space-between; */
}
.footer-container:lang(ar) {
  direction: rtl;
}
.footer-container:lang(en) {
  direction: ltr;
}

@media only screen and (max-width: 700px) {
  .footer-container {
    gap: 30px;
  }
}

.footer-container > * {
}
.more-in-home > p,
.about-somo > p,
.contact-us > p {
  font-weight: 900;
  font-size: 1rem;
}
.more-in-home ul,
.about-somo ul,
.contact-us ul {
  padding: 0;
}
.more-in-home ul > li,
.about-somo ul > li,
.contact-us ul > li {
  list-style: none;
}
.more-in-home ul > li > a,
.about-somo ul > li > a,
.contact-us ul > li > a {
  color: #000;
  text-decoration: none;
  font-size: 0.8rem;
}
.line-horizonatl {
  display: flex;
  background-color: rgb(100, 100, 100);
  height: 90%;
  width: 1px;
}
.contact-us {
  flex-grow: 1;
  /* width: ; */
}
.contact-us ul > li i {
  font-size: 1.5rem;
}
.contact-us > ul {
  display: flex;
  gap: 20px;
}
</style>
