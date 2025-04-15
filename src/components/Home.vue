<template>
  <h1>HomePage</h1>
  
  <ul>
    <li v-for="items in getContact" :key="items.name">
      <Users :data="items" :getPhone="getData"/>
    </li>
  </ul>
</template>

<script>
import Users from "./Users.vue";
export default {
  name: "HomePage",
  components: {
    Users,
  },
  data() {
    return {
      userData: {
        name: "Araf",
        email: "Araf@gmail.com",
      },
      getContact: [
        { name: "Araf", phone: "01711111111" },
        { name: "Zara", phone: "01712222222" },
        { name: "Imran", phone: "01713333333" },
        { name: "Lamia", phone: "01714444444" },
        { name: "Tanvir", phone: "01715555555" },
        { name: "Sadia", phone: "01716666666" },
        { name: "Rafi", phone: "01717777777" },
        { name: "Nadia", phone: "01718888888" },
        { name: "Hasan", phone: "01719999999" },
        { name: "Mira", phone: "01710000000" },
      ],
    };
  },
  methods: {
    getData(phone) {
      alert(`phone number is ${phone}`);
    },
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
