<template>
  <h1>HomePage</h1>
    <h2 v-if="show">If Condition</h2>
    <h2 v-else>Else Condition</h2>
    <button v-on:click="show=!show">Toggle</button>
</template>

<script>
export default {
  name: "HomePage",
    data(){
        return{
            show:true,
        }
    }
};
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
