<template>
  <div v-bind="$attrs">
    <h1>Ibrahim</h1>
    <h1>Araf</h1>
    <h1>Masud</h1>
    <h1>{{ data }}</h1>

    <h1>Total: {{getResult}} </h1>
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
        dollar:120,
        takaVal:100,
        discount:35

    }
  },
  computed:{
    getResult(){
        return (this.dollar*this.takaVal)-this.discount;
    }
  }
};
</script>
<style scoped></style>

<!-- Computed property: simply for cache works. like if a value will not change for a long time then its being used. when the value will be updated in that case it will automatically re-cache the original one -->