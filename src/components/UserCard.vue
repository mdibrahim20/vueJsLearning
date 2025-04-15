<template>

<div class="card" v-on:click="sendMessageToParent">
    <h2>Name: {{ name }}</h2>
    <p>Email: {{ email }}</p>
    <p :class="{active:isActive}">Status: {{ isActive?'Active':"Inactive" }}</p>
</div>

</template>
<script>
export default{
    name:"UserCard",
    props:['name','email','isActive'],
    methods:{
        sendMessageToParent(){
            this.$emit('user-clicked',`${this.name} card clicked`)
        }
    }
}
</script>
<style scoped>
.card {
  border: 1px solid #ddd;
  padding: 15px;
  margin: 10px;
  border-radius: 8px;
  cursor: pointer;
}
.active {
  color: green;
}
</style>