<template>
  <ChildComp><h1>Ibrahim</h1></ChildComp>
  <ChildComp><a href="#">www.google.com</a></ChildComp>
  <ChildComp><img src="https://thafd.bing.com/th/id/OIP.0iqvqUM-_MntTZp4CMBaigHaEK?cb=iwp1&rs=1&pid=ImgDetMain"/></ChildComp>
  <ChildComp></ChildComp>
</template>

<script>

import ChildComp from "./ChildCom.vue";
export default {
  name: "HomePage",
  components: {

    ChildComp
  },
};
</script>

<style scoped></style>
