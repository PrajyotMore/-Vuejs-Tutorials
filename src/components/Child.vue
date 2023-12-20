<template>
<h1>{{name}} component</h1>
<p>{{object.pincode}}</p>

<button v-on:click="passData()">child</button>
<ul>
<li v-for="item in edata" :key="item.name">
<SubChild  :item="item" :getInformation="getInformation"/>
</li>
</ul>

<!-- applying styles dynamically on base of btn click -->
<h6 :class="applyStyle">WE ARE WELCOME FOR VUE JS</h6>
<button v-on:click="colorfull=!colorfull">Apply style</button>
<!-- applying styles dynamically on base of btn click -->

<div v-html="tag">

</div>

</template>

<script>

import SubChild from "./SubChild.vue"
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Child',
    components: {
        SubChild
    },
    data() {
        return {
            edata: [{
                    name: 'prajyot',
                    address: 'panvel',
                    gender: 'male',
                },
                {
                    name: 'diksha',
                    address: 'thane',
                    gender: 'female'
                },
                {
                    name: 'ehsan',
                    address: 'bhandup',
                    gender: 'male'
                },
                {
                    name: 'vikrant',
                    address: 'Parel',
                    gender: 'male'
                },

            ],
            tag:"<p>Hello Vue js</p>",
            colorfull:false,
        }
    },
    computed:{
        applyStyle(){
            return {
                green: this.colorfull,
                err: false,
                other: true
            }
        }
    },
    methods:{
        getInformation(name) {
            alert(name)
        }
    },
    props: {
        name: String,
        object: Object,
        passData: Function
    }
}
</script>

<style>
.green{
    background-color:green;
    color:white;
    width:200px;
    padding:20px;
}
.err{
    color:red;
}
.other{
    color:yellow;
}
</style>
