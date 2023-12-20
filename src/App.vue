<template>
  <HelloWorld msg="Welcome to Vue js coding"/>
  <Home/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Home from './components/Home.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Home,
  }
}
</script>


