<template>

<div class="info">
    <h2 > voici les nom des etudiants de l'informatique </h2>
        <div v-for="(item,i) in info" v-bind:key="i">
            
        <p v-if="item.spe == 'informatique'">{{item.id}}-- {{item.nom}} 
            <span>
                <button v-on:click="deleteInfo(item.nom)">
                     delete frr
                </button>
                
            </span> </p>

        </div>
</div>

</template>

<script>
export default {
    name:"info",
    props:["info"],
    methods:{
       deleteInfo(name){
            this.$emit('delete',{name}) 
          
       }
      
    }
}
</script>

<style>


</style>




























