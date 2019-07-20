<template>
  <div id="contact" class="mb-5">
    <h1 class="display-1 font-weight-bold mb-3">Contact me</h1>
    <p>Igor Jerosimić</p>
    <p>47000 Karlovac</p>
    <p>Croatia</p>
    <p @click="email()" id="email">
      <b>igor.jerosimic1@gmail.com</b>
    </p>
    <p>
      <b>+385 97 680 93 98</b>
    </p>
    <h1 class="display-1 font-weight-bold mb-3 mt-5">Or check out my...</h1>
    <v-layout justify-center v-bind="buttons">
      <v-btn
        outline
        color="indigo"
        v-for="(link, i) in importantLinks"
        :key="i"
        :href="link.href"
        class="subheading mx-3"
        target="_blank"
      >{{ link.text }}</v-btn>
    </v-layout>
  </div>
</template>

<script>
export default {
  data: () => ({
    importantLinks: [
      {
        text: "CV",
        href: "https://ijerosimic.github.io/CV.pdf"
      },
      {
        text: "GitHub",
        href: "https://github.com/ijerosimic"
      },
      {
        text: "LinkedIn",
        href: "https://www.linkedin.com/in/ijerosimic/"
      }
    ]
  }),
  methods: {
    email() {
      window.location.href = "mailto:igor.jerosimic1@gmail.com";
    }
  },
  computed: {
    buttons() {
      const buttons = {};
      if (this.$vuetify.breakpoint.xsOnly) buttons.column = true;

      return buttons;
    }
  }
};
</script>

<style>
</style>
