<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld />
  <Seba />
  <info1 v-bind:info="students" @delete="deletStudents" />  
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
      students:[{id:1,nom:"Seba",spe:"informatique"},
                 {id:2,nom:"yagoubi",spe:"informatique"},
                 {id:3,nom:"hannachi",spe:"electronique"},
                 {id:4,nom:"gherras",spe:"electronique"},
                 {id:5,nom:"bob",spe:"informatique"} 
      ]
    }
  },
  methods:{
       deletStudents(name){
          this.students = this.students.filter(student => {
            return student.nom != name.name
          })

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
