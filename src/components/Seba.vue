<template>
    
  <div>
   
<h1> {{message}}</h1>
<h1> {{message2}}</h1>
 <button @click="changeMsg">changer le </button>    <!-- --> 
  </div>

</template>

<script>
export default {
  name:"seba",
  data(){

     return{ 
        message:"SEBA bienvenue",
        message2:"Hello"
     }

  },
  methods:{
        changeMsg(){
          this.message2="hello everybody"
        }
  },
  created(){

      alert("created")

  },
  beforeCreate(){
       
       alert("before created")  
  },
  beforeUpdate(){
    alert("before update")
  }
}
</script>

<style>

</style>


























