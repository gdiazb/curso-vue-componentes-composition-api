<template>
  <div>
    <p>{{ text }}</p>
    <p>{{ nombre }}</p>
  </div>
</template>

<script>
import base from "@/mixins/base";

export default {
  name: "App",
  mixins: [base],
  data() {
    return {
      text: "Hola mor",
    };
  },
  beforeCreate() {
    console.log("beforeCreate", this.text);
  },
  created() {
    console.log("created", this.text);
  },
  mounted() {
    console.log("mounted", this.text);
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
