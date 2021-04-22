<template>
    
  <div>
   
<h1> {{message}}</h1>
<h1> {{message2}}</h1>
 <button @click="changeMsg">changer le </button>    <!-- --> 
  </div>
  <div class="posts" v-for="(post,id) in posts" :key="id">
  <h2>{{post.title}}</h2>
   <p>{{post.body}}</p>
   
  </div>

</template> 

<script>
import axios from '../../node_modules/axios'
//import axios1 from 'axios'
export default {
  name:"seba",
  data(){

     return{ 
        message:"SEBA bienvenue",
        message2:"Hello",
        posts:[]
     }

  },
  methods:{
        changeMsg(){
          this.message2="hello everybody"
        }
  },
  created(){

     // alert("created")
      axios.get("https://jsonplaceholder.typicode.com/posts")
      .then(x=>{
       // console.log(x.data);
        this.posts=x.data
      }).catch(e=>{
           console.log(e+"aaaaaezaeaeaze")
          // document.write(e+"azerr")
           
      })
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


























