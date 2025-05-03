<template>
  <h1>Ref uses vue</h1>
  <input type="text" ref="input" />
  <Form></Form>
  <UserComp data="Ibrahim Khalil" id="test-id"></UserComp>
</template>

<script>
import Form from "./FormCompo";
import UserComp from "./User.vue";
export default {
  name: "HomePage",
  components: {
    Form,
    UserComp
  },
};
</script>

<style scoped></style>
