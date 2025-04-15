<template>
  <h1>HomePage</h1>

  <div>
    <h1 :class="{green:colorful}">Class Binding</h1>
    <button v-on:click="colorful=!colorful">Click Me</button>
  </div>

</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
      colorful:true,
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

.green{
  background-color: green;
  padding: 20px;
  width: 200px;
  height: 50px;
  border-radius: 10px;
}

.red{
  color: red;
}
</style>
