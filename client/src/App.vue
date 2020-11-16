<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
      src="https://picsum.photos/id/459/1920/1080"
    >
      <div class="d-flex align-center">
        <a href="/">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/logoup.png"
          transition="scale-transition"
          width="40"
        />
        </a>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        to="Jobs"
        text
      >
        <span class="mr-2">Jobs</span>
      </v-btn>
      <v-btn
        to="Food"
        text
      >
        <span class="mr-2">Food</span>
      </v-btn>
    </v-app-bar>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>
