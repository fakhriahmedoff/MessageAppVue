<template>
  <div>
    <div class="mail-container">
      <h1>Enter email</h1>
      <input
        v-model="email"
        class="form-control"
        placeholder="Email"
        required
      />
      <div class="buttons">
        <MyBtn @click="send()" :loading="load" :count="1" />
        <MyBtn :count="10" />
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import MyBtn from "./components/Button.vue";
import "./assets/styles/style.css";

export default {
  name: "App",
  components: {
    MyBtn,
  },
  data() {
    return {
      email: "",
      load: false,
    };
  },
  methods: {
    send() {
      axios
        .post("https://jsonplaceholder.typicode.com/todos/1", {
          email: this.email,
        })
        .then(function (response) {
          console.log(response);
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },
};
</script>
