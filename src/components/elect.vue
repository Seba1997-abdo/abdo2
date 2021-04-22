<template>

<div class="elect">
    <h2 > voici les nom des etudiants de l'electronique </h2>
        <div v-for="(item,i) in elect" v-bind:key="i">
            
        <p v-if="item.spe == 'electronique'">{{item.id}} -- {{item.nom}}</p> 

        </div>
</div>

</template>

<script>
export default {
    name:"elect",
    props:["elect"] 

}
</script>

<style>


</style>




















