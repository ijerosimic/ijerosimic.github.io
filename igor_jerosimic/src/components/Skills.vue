<template>
  <div id="skills">
    <h1 class="display-1 font-weight-bold mb-3">Stack</h1>
    <v-flex lg6 xs12 offset-lg3>
      <v-layout row v-bind="stackList">
        <v-flex v-for="(skill, i) in skills" :key="i" xs4>
          <u>
            <p>{{ skill.group }}</p>
          </u>
          <ul>
            <li v-for="(tech, i) in skill.stack" :key="i">
              <p>{{tech}}</p>
            </li>
          </ul>
        </v-flex>
      </v-layout>
    </v-flex>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      skills: [
        {
          group: "Professional experience",
          stack: [
            ".NET Core (C#, ASP.NET MVC, Web API, EntityFramework)",
            "MS SQL Server",
            "Javascript",
            "HTML",
            "CSS"
          ]
        },
        {
          group: "Some experience with",
          stack: ["Postman", "MS Azure"]
        },
        {
          group: "Personal experience",
          stack: ["Node.js", "Vue.js", "RabbitMQ", "xUnit"]
        }
      ]
    };
  },
  computed: {
    stackList() {
      const stackList = {};
      if (this.$vuetify.breakpoint.mdAndDown) stackList.column = true;

      return stackList;
    }
  }
};
</script>

<style>
</style>
