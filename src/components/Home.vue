<template>
<div>
  <h1>User Cards</h1>
  <UserCard v-for="(user) in users" :key="user.email" :name="user.name" :email="user.email" :isActive="user.active" @user-clicked="handleUserClick"/>
  <h3>{{ message }}</h3>
</div>

</template>

<script>
import UserCard from './UserCard.vue';
export default {
  name: "HomePage",
  components:{
    UserCard
  },
  data(){
    return{
      users: [
        { name: 'Ibrahim', email: 'ibrahim@vue.com', active: true },
        { name: 'Zanin', email: 'zanin@vue.com', active: false },
        { name: 'Araf', email: 'araf@vue.com', active: true },
      ],
      message:""
    }
  },
  methods:{
    handleUserClick(msg){
      this.message = msg;
    }
  }

}
</script>

<style scoped>

</style>
