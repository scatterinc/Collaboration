<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">Grid Issue</router-link> |
      <router-link to="/problemone">Problem1</router-link> |
      <router-link to="/problemtwo">Problem 2</router-link>
    </div>
    <router-view />
    <modal-center />
  </div>
</template>

<script>
import ModalCenter from "./components/Modaltest.vue";

export default {
  components: { ModalCenter },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
