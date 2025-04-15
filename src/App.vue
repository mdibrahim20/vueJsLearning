<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
   <Home/>
  <Project/>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home,
  }
}
</script>