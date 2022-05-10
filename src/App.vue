<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <button @click="logout">Logout</button>
  <p v-font-size:small>Small</p>
  <p v-font-size:Medium>Medium</p>
  <p v-font-size:Large>Large</p>
  <div>
    <MyHeader/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import { inject } from "vue";

export default {
  name: "App",
  components: {
    // HelloWorld
  },
  setup() {
    const logout = inject("logout");

    return {
      logout,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
