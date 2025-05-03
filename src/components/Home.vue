<template>
  <ChildComp>
    <template v-slot:header>
      <h1>Google</h1>
    </template>
    <template v-slot:main>
      <img src="https://thafd.bing.com/th/id/OIP.URPfXjbxMgRsxwxpTdBm5AHaG0?cb=iwp1&rs=1&pid=ImgDetMain" width="200px"/>
      <h1>this is main / content part</h1>
    </template>
    <template v-slot:footer>
      <h1>This is footer</h1>
    </template>
  </ChildComp>
  <ChildComp>
    <template v-slot:header>
      <h1>Youtube</h1>
    </template>
    <template v-slot:main>
      <img src="https://thafd.bing.com/th/id/OIP.URPfXjbxMgRsxwxpTdBm5AHaG0?cb=iwp1&rs=1&pid=ImgDetMain" width="200px"/>
      <h1>this is main / content part</h1>
    </template>
    <template v-slot:footer>
      <h1>This is footer</h1>
    </template>
  </ChildComp>
  <ChildComp>
    <template v-slot:header>
      <h1>Facebook</h1>
    </template>
    <template v-slot:main>
      <img src="https://thafd.bing.com/th/id/OIP.URPfXjbxMgRsxwxpTdBm5AHaG0?cb=iwp1&rs=1&pid=ImgDetMain" width="100px"/>
      <h1>this is main / content part</h1>
    </template>
    <template v-slot:footer>
  
    </template>
  </ChildComp>
</template>

<script>
import ChildComp from "./ChildCom.vue";
export default {
  name: "HomePage",
  components: {
    ChildComp,
  },
};
</script>

<style scoped></style>
