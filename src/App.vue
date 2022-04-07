<template>
  <div>
    <div class="mail-container">
      <h1>Enter email</h1>
       {{email}}
      <input v-model="email" class="form-control" placeholder="Email" required />
      <div class="buttons">
        <MyBtn @click="send()"  :count="1" />
        <MyBtn :count="10" />
      </div>

    </div>
  </div>
</template>

<script>
import MyBtn from "./components/Button.vue";
import './assets/styles/style.css';

export default {
  name: "App",
  components: {
    MyBtn,
  },
  data() {
    return {
      email: ''
    }
  },
  methods: {
    send() {
      
    },
  },
};
</script>
