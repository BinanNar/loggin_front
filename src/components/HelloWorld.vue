<template>
  <v-container fluid>
    <v-row justify="center">
      <h1>hola</h1>
    </v-row>
    <v-row justify="center">
      <v-btn v-on:click="logingoogle()">login con microsoft XD</v-btn>
    </v-row>
  </v-container>
</template>

<script>
import axios from "axios";

export default {
  name: "HelloWorld",

  data: () => ({}),

  methods: {
    logingoogle() {
      axios
        .get("http://127.0.0.1:8000/signin")
        .then((res) => { console.log(res.data)
          window.location.href = res.data.link
        })
        .catch((err) => {});
    },
  },
};
</script>
