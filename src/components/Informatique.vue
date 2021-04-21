<template>

<div class="info">
    <h2 > voici les nom des etudiants de l'informatique </h2>
        <div v-for="(item,i) in info" v-bind:key="i">
            
        <p v-if="item.spe == 'informatique'">-- {{item.nom}}</p>

        </div>
</div>

</template>

<script>
export default {
    name:"info",
    props:["info"]
}
</script>

<style>


</style>




























