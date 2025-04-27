<template>
  <h1>Ref uses vue</h1>
  <input type="text" ref="input" />
  <Form></Form>
</template>

<script>
import Form from "./FormCompo";
export default {
  name: "HomePage",
  components: {
    Form,
  },
};
</script>

<style scoped></style>
