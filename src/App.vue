<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld />
  <Seba />
  <info1 v-bind:info="students" /> 
  <elec1 v-bind:elect="students" />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Seba from "./components/Seba.vue";
import info1 from "./components/Informatique.vue";
import elec1 from "./components/elect.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Seba,
    info1,
    elec1
  },
  data() {
    return {
      students:[{nom:"Seba",spe:"informatique"},
                 {nom:"yagoubi",spe:"informatique"},
                 {nom:"hannachi",spe:"electronique"},
                 {nom:"gherras",spe:"electronique"},
                 {nom:"bob",spe:"informatique"}
      ]
    }
  }
}
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
