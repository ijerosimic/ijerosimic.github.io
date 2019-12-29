<template>
  <div id="app">
    <v-flex xs12 mt-3 mb-5 id="top">
      <v-btn flat="flat" @click="$vuetify.goTo('#about')">about</v-btn>
      <v-btn flat="flat" @click="$vuetify.goTo('#skills')">stack</v-btn>
      <v-btn flat="flat" @click="$vuetify.goTo('#contact')">contact me</v-btn>
      <v-btn flat="flat" href="https://ijerosimic.github.io/IgorJerosimic.pdf" target="_blank">CV</v-btn>
      <v-btn flat="flat" href="https://github.com/ijerosimic" target="_blank">GitHub</v-btn>
      <v-btn flat="flat" href="https://www.linkedin.com/in/ijerosimic/" target="_blank">LinkedIn</v-btn>
    </v-flex>
    <IgorJerosimic msg="Welcome to my personal page." />
    <v-flex xs12 mb-5 mt-5>
      <v-layout justify-center>
        <v-btn flat="flat" @click="$vuetify.goTo('#top')">Back to top</v-btn>
      </v-layout>
    </v-flex>
  </div>
</template>

<script>
import IgorJerosimic from "./components/IgorJerosimic.vue";

export default {
  name: "app",
  components: {
    IgorJerosimic
  }
};
</script>

<style>
#app {
  font-family: "Consolas";
  font-size: 14px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 3rem;
}
ul {
  list-style-type: none;
}
#email {
  cursor: pointer;
}
</style>
