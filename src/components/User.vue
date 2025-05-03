<template>
  <div v-bind="$attrs">
    <h1>Ibrahim</h1>
    <h1>Araf</h1>
    <h1>Masud</h1>
    <h1>{{ data }}</h1>
  </div>
</template>
<script>
export default {
  name: "UserComp",
  props: {
    data:String,
    id:String,
  },
};
</script>
<style scoped></style>
