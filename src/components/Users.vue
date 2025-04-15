<template>
<ul class="contact-list">
  <li class="contact-item">
    <div class="contact-card">
      <p class="contact-name">{{ data.name }}</p>
      <p class="contact-phone">{{ data.phone }}</p>
      <button v-on:click="getPhone(data.phone)">Phone Number</button>
    </div>
    
  </li>
</ul>

</template>
<script>
export default{
    name:"UsersComponent",
    props:{
        data:Object,
        getPhone:Function,
    }
}
</script>
<style scoped>
.contact-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.contact-item {
  margin-bottom: 1rem;
}

.contact-card {
  background-color: #f5f5f5;
  border-radius: 12px;
  padding: 15px 20px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

.contact-card:hover {
  transform: scale(1.02);
}

.contact-name {
  font-weight: bold;
  font-size: 18px;
  margin: 0 0 5px 0;
  color: #333;
}

.contact-phone {
  font-size: 14px;
  color: #666;
  margin: 0;
}
</style>
