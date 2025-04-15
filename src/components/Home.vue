<template>
  <h1>HomePage</h1>
<Child name="Md Ibrahim Khalil" :details="userData" :functionCall="getData"/>
</template>

<script>
import Child from './Child.vue';
export default {
  name: "HomePage",
  components:{
    Child
  },
  data(){
    return{
      userData:{
        name:"Araf",email:"Araf@gmail.com"
      }
    }
  },
  methods:{
    getData(){
      alert("Invoked from parent component")
    }
  }

}
</script>

<style scoped>
h1,
h2 {
  color: red;
}
h2 {
  font-size: 50px;
}
</style>
