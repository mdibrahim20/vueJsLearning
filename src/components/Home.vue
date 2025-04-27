<template>

    <h1>Ref uses vue</h1>
    <input type="text" ref="input" />
    <button v-on:click="getData">Click Me</button>

</template>

<script>
export default {
  name: "HomePage",
  methods: {
    getData() {
      this.$refs.input.focus();
      let val = this.$refs.input.value;
      console.log(val)
      this.$refs.input.style.color='red';
    }
  },
};
</script>

<style scoped></style>
