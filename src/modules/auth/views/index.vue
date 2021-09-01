<script>
export default {
  name: "index",

  data: () => ({
    model: {}
  }),

  methods: {
    logIn() {
      localStorage.setItem("credentials", JSON.stringify({token: 123}))
    }
  }
}
</script>

<template>
  <div class="d-flex align-center justify-center full-height">
    <v-card>
      <v-card-title>
        Authorization
      </v-card-title>
      <v-card-text>
        <v-text-field lable="login" v-model="model.login"/>
        <v-text-field lable="password" v-model="model.password"/>
        <v-btn link to="/information-general" @click="logIn">
          login
        </v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<style scoped>
.full-width {
  width: 100%;
}
.full-height {
  height: 100%;
}
</style>