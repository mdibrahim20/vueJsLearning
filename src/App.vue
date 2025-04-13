<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <!-- <HomePage/> -->
  <Project/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import HomePage from './components/Home.vue'
import Project from './components/Project.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    // HomePage,
    Project,

  }
}
</script>