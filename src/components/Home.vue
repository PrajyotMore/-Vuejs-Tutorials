<template>

<h1 v-on:mousemove="getConsole()">Home Component</h1>
<!-- <h1>Email {{email}}</h1>
<h1>Mobile {{mobile==8888}}</h1>
<h1>Function Name {{getData("Vue js")}}</h1>
<h1>Array {{array}}</h1>
<button v-on:click="getCount()">Count Me</button>
<h1>object {{object.pincode}}</h1>
<h1>Address {{getAddress()}} </h1>
<button v-on:click="getBData('button clicked 1')">Click Me</button>
<button v-on:dblclick="getDData('button double clicked')">Click Me</button>
<button v-on:click="getCount()">Count Me</button>
<h2>{{count}}</h2> -->


<!-- Parent to child passing data-->
<Child name="prajyot" :object="object" :passData="passData"/>
<!-- Parent to child passing data-->



<!-- Two way Binding -->
<!-- <input type="text" v-model='counter'/>
<h2>{{counter}}</h2> -->
<!-- Two way Binding -->

<!-- Gettting values from input field with two way binding  -->
<!-- <input type="text" placeholder="enter email" v-model='email'/>
<br/>
<br/>
<input type="password" placeholder="enter password" v-model='password'/>
<br/>
<br/>
<button v-on:click='getValues()' type="button">Get Values</button> -->

<!-- Gettting values from input field with two way binding  -->

<!-- Get Checkbox & Radio button values -->

<!-- <h3>Technology</h3>
<label for="javascript">javascript</label>
<input type="checkbox" value="javascript" v-model="technology" id="javascript" />
<label for="html">html</label>
<input type="checkbox" value="html" v-model='technology' id="html" />
<label for="css">css</label>
<input type="checkbox" value="css" v-model='technology' id="css" />
<label for="React">React</label>
<input type="checkbox" value="React" v-model='technology' id="React" />

<h4>Selected technology : {{technology}}</h4>

<br />
<br />

<h3>who i am ?</h3>
<label for="student">student</label>
<input type="radio" value="student" v-model="profession" name="profession" id="student" />

<label for="developer">Developer</label>
<input type="radio" value="developer" v-model="profession" name="profession" id="developer" />

<h4>I am : {{profession}}</h4> -->

<!-- Get Checkbox & Radio button values -->

<!-- if else condition with toggle -->

<!-- <h1 v-if="show">If Condition</h1>
<h1 v-else>Else Condition</h1>

<button v-on:click="show=!show">Toggle</button> -->

<!-- if else condition with toggle -->

<!-- appliyng loop in array and array of object  -->

<h1>loop in array and array of object</h1>

<ul>
    <li v-for="item in number" :key="item">
        {{item}}
    </li>


    <br/>
    <br/>

<ul>
<li v-for="el in userData" :key="el.name">
Name : {{el.name}} and City : {{el.city}}
</li>
</ul>

</ul>

<!-- appliyng loop in array and array of object  -->

</template>

<script>
import Child from "./Child.vue";
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Home',
    components: {
        Child,
    },
    data() {
        return {
            email: null,
            password: null,
            mobile: 7385512964,
            getData(a) {
                return a
            },
            array: [],
            object: {
                pincode: 421503,
                area: "badlapur"
            },
            count: 0,
            counter: 10,
            technology: [],
            profession: null,
            show: true,
            number: [1, 2, 3, 57, 77, 8, 3, 5],
            userData:[{
                name:'prajyot',
                city:'mumbai'
            },{
                name:'prathamesh',
                city:'kolhapur'
            },{
                name:'vivek',
                city:'thane'
            }]
        }

    },
    methods: {
        getAddress() {
            return {
                add: 'kjvjsddjvkfj',
                email: this.email
            }
        },
        getBData(data) {

            alert(data)
        },
        getDData(data) {

            alert(data)
        },
        getConsole() {
            console.log('hovered on h2 home component')
        },
        getCount() {
            // this.count = this.count + 1;
            this.array = this.array + 1;
        },
        getValues() {
            console.log('input form values are', this.email, this.password)
        },
        passData(){
            console.log('Calling from parent component')
        }
    }
}
</script> 

<style scoped>
h1 {
    color: orange
}
</style>
