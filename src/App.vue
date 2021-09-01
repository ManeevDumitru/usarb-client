<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),

  computed: {
    user() {
      return localStorage.getItem("credentials");
    }
  }
};
</script>

<template>
  <v-app>
    <v-app-bar app v-if="user">
      test
    </v-app-bar>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>
