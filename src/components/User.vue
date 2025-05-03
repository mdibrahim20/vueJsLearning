<template>
  <div v-bind="$attrs">
    <h1>Ibrahim</h1>
    <h1>Araf</h1>
    <h1>Masud</h1>
    <h1>{{ data }}</h1>

    <h1>Count : {{ count  }} </h1>
    <button @click="count=count+1">+</button>
    <button @click="count=count-1">-</button>
  </div>
</template>
<script>
export default {
  name: "UserComp",
  props: {
    data:String,
    id:String,
  },
  data(){
    return{
        count:0,
    }
  },
  watch:{
    count(val,prev){
        // if(val>5){
        //     alert("stop")
        // }
        // if(val>5 && val>prev){
        //     this.count=0;
        //     alert("value turn to 0")
        // }
        if(val>5){
            alert(prev)
        }
    }
  }

};
</script>
<style scoped></style>
