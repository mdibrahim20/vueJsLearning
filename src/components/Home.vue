<template>
  <h1>HomePage</h1>
  <h1>For Loops</h1>
  <ul>
    <li v-for="items in technology" :key="items">
        {{ items }}
    </li>
  </ul>
  <h2>User Details</h2>
  <ul>
    <li v-for="items in userDetails" :key="items.email">
        {{ items.name }} his email is {{ items.email }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
        technology:["A","B","C","D","E"],
        userDetails:[{
            name:"Araf",
            email:"a@b.com"
        },
        {
            name:"Ibrahim",
            email:"Ibrahim@b.com"
        },
        {
            name:"Dihan",
            email:"Dihan@b.com"
        },
        {
            name:"Masud",
            email:"Masud@b.com"
        },
        {
            name:"Zanin",
            email:"Zanin@b.com"
        },
    ]
    };
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
