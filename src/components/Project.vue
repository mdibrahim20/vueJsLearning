<template>
  <div class="contact-manager">
    <h1>Contact Manager</h1>

    <!-- Add Contact Form -->
     <div class="form">
        <input type="text" v-model="name" placeholder="Enter your name">
        <input type="email" v-model="email" placeholder="Enter your email">
        <button v-on:click="addContact()">Add Contact</button>
     </div>

     <!-- Error Message -->
     <p v-if="errorMessage" class="error">{{ errorMessage }}</p>
     <p v-else-if="successMessage" class="success">{{ successMessage }}</p>
     <!-- Contact List -->
      <h1>Contact List</h1>
      <ul v-if="contacts.length>0">
        <li v-for="(items,index) in contacts" :key="items.email">
            {{ items.name }} - {{ items.email }}
            <button v-on:click="deleteContact(index)">❌ Delete</button>
        </li>
      </ul>
      <p v-else>No contacts found</p>
  </div>
</template>

<script>
export default {
  name: "ProjectData",
  data(){
    return{
        name:"",
        email:"",
        contacts:[],
        errorMessage:"",
        successMessage:""
    }
  },
  methods:{
    addContact(){
        if(!this.name || !this.email){
            this.errorMessage = "Both fields are required";
            this.successMessage=""
            return;
        }

        // Prevent Duplicate emails
        const exist = this.contacts.some(c=>c.email===this.email);
        if(exist){
            this.errorMessage="Email already Exists";
            this.successMessage="";
            return;
        }

        this.contacts.push({name:this.name,email:this.email});
        this.name="";
        this.email="";
        this.successMessage="Contact Added Successfully";
        this.errorMessage="";
    },
    deleteContact(index){
        this.contacts.splice(index,1);
        this.successMessage="Contact Deleted";
        this.errorMessage="";
    }
  }
};
</script>
<style scoped>
.contact-manager {
  max-width: 500px;
  margin: auto;
  padding: 20px;
  font-family: sans-serif;
}
input {
  padding: 8px;
  margin: 5px;
  width: 45%;
}
button {
  padding: 8px 12px;
  margin-top: 10px;
}
.error {
  color: red;
}
.success {
  color: green;
}
li {
  margin: 10px 0;
}
</style>
