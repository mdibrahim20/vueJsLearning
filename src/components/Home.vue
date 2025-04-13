<template>
  <h1 v-on:mousemove="getConsole()">HomePage</h1>
  <button v-on:click="clickMe('Button 1')">Button 1</button>
  <button v-on:dblclick="dblClicked('Button 2')">Button 2</button>
  <button v-on:click="countIncrease()">Count +</button>
  <h2>{{ count }}</h2>
</template>

<script>
export default {
  name: "HomePage",
  data(){
    return{
        count:0
    }
  },
  methods: {
    clickMe(txt){
        alert(`${txt} has been clicked`)
    },
    dblClicked(txt){
        alert(`${txt} has been double clicked`)
    },
    getConsole(){
        console.warn("Mouse move detected");
        
    },
    countIncrease(){
        this.count = this.count+1;
    }
  },
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
