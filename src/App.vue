<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Hello-i18n />
  </div>
</template>

<script>
import HelloI18n from "./components/HelloI18n.vue";

export default {
  name: "App",
  components: {
    HelloI18n,
  },
  created() {
    const lang = localStorage.getItem("lang");
    if (lang) {
      this.$i18n.locale = lang;
    }
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
