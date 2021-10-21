<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key="index">{{index}}. {{data.skill}}</li>
      </ul>

      <p v-if="skills.length >= 1">You have more than 1 skills</p>
      <p v-else>You have 0 skills</p>
    </div>
    {{ name }}

    {{ btnState ? "The button is disabled" : "The button is active" }}

    <button v-on:click="changeName" v-bind:disabled="btnState">
      Change Name
    </button>
  </div>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      name: "Coursetro",
      btnState: true,
      skills: [
        { skill: "Vue.js" },
        { skill: "Frontend Developer" },
        ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped>

</style>
