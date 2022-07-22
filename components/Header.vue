<template>
  <v-container>
    <v-toolbar flat class="mainHeader">
      <v-toolbar-title>
         <v-avatar>
            <img src="../assets/images/logo11.jpeg" alt="John" />
          </v-avatar>
        ALNAHRAIN EVENT
        </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-btn text><nuxt-link to="/">Home</nuxt-link></v-btn>
        <v-btn text><nuxt-link to="/event">Event</nuxt-link></v-btn>
        <v-btn text><nuxt-link to="/">Contact Us</nuxt-link></v-btn>
        <v-btn text>
          <v-avatar>
            <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
          </v-avatar>
        </v-btn>
      </v-toolbar-items>
      <div class="hidden-sm-and-up">
        <v-menu offset-y>
          <template v-slot:activator="{ on }">
            <v-app-bar-nav-icon v-on="on"></v-app-bar-nav-icon>
          </template>
          <v-list class="responsiveMenu">
            <v-list-item>
              <v-list-item-title to="/event">Event</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>About</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-list-item-title>Contact</v-list-item-title>
            </v-list-item>

            <v-list-item>
              <v-avatar>
                <img
                  src="https://cdn.vuetifyjs.com/images/john.jpg"
                  alt="John"
                />
              </v-avatar>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
  name: "Header",
  data: () => ({}),
};
</script>


