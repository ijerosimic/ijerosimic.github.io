<template>
  <v-container>
    <v-avatar size="300px">
      <img src="../assets/igor.png" />
    </v-avatar>
    <About class="mt-5" />
    <Skills class="mt-5" />
    <Contact class="mt-3" />
  </v-container>
</template>

<script>
import About from "./About";
import Skills from "./Skills.vue";
import Contact from "./Contact.vue";
export default {
  components: {
    About,
    Skills,
    Contact
  }
};
</script>

<style>
</style>


