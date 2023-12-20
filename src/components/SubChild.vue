<template>
<div class="wrapper">
<h4>{{item.name}}</h4>
<h4>{{item.address}}</h4>
<h4>{{item.gender}}</h4>
<button v-on:click="getInformation(item.name)">Click me</button>
</div>



</template>

<script>
export default {
    name: "SubChild",
    props: {
        item: Object,
        getInformation:Function
    },
    
}


</script>

<style>

.wrapper{
    background-color: lightblue;
    padding: 10px;
    border-bottom: 2px solid lightseagreen;
    margin-bottom: 20px;
}
</style>