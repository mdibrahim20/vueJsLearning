<template>
    <div class="form-container">
      <h1>Form with Validation</h1>
      
      <div class="form-debug">
        {{ form }}
      </div>
  
      <ul v-if="error.length" class="error-list">
        <li v-for="item in error" :key="item">
          {{ item }} is not valid
        </li>
      </ul>
  
      <form @submit.prevent="Login" class="form-content">
        <div class="form-group">
          <label>Email</label>
          <input type="email" v-model.trim.lazy="form.email" />
        </div>
  
        <div class="form-group">
          <label>Password</label>
          <input type="password" v-model.trim.lazy="form.password" />
        </div>
  
        <div class="form-group">
          <label>Country</label>
          <select v-model.trim.lazy="form.country">
            <option disabled value="">Select your country</option>
            <option>Bangladesh</option>
            <option>India</option>
            <option>Nepal</option>
            <option>Bhutan</option>
          </select>
        </div>
  
        <div class="form-group">
          <label>Technologies</label>
          <div class="checkbox-group">
            <label><input type="checkbox" value="java" v-model.trim.lazy="form.technology" /> Java</label>
            <label><input type="checkbox" value="kotlin" v-model.trim.lazy="form.technology" /> Kotlin</label>
            <label><input type="checkbox" value="python" v-model.trim.lazy="form.technology" /> Python</label>
          </div>
        </div>
  
        <div class="form-group">
          <label>Gender</label>
          <div class="radio-group">
            <label><input type="radio" name="gender" value="Male" v-model.trim.lazy="form.gender" /> Male</label>
            <label><input type="radio" name="gender" value="Female" v-model.trim.lazy="form.gender" /> Female</label>
          </div>
        </div>
  
        <button type="submit" class="submit-btn">Login</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: "FormCompo",
    data() {
      return {
        form: {
          email: "",
          password: "",
          country: "",
          technology: [],
          gender: ""
        },
        error: []
      };
    },
    methods: {
      Login() {
        this.error = [];
        for (const item in this.form) {
          if (this.form[item] === "" || this.form[item].length === 0) {
            this.error.push(item);
          }
        }
        if (this.error.length === 0) {
          alert("Form has been submitted");
        }
        console.warn(this.form, this.error);
      }
    }
  };
  </script>
  
  <style scoped>
  .form-container {
    max-width: 500px;
    margin: 50px auto;
    padding: 30px;
    background: #f9f9f9;
    box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
    border-radius: 12px;
    font-family: Arial, sans-serif;
  }
  
  .form-container h1 {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .form-debug {
    font-size: 12px;
    color: #666;
    margin-bottom: 20px;
    word-break: break-word;
  }
  
  .error-list {
    background: #ffe0e0;
    color: #d8000c;
    border: 1px solid #d8000c;
    padding: 10px;
    border-radius: 8px;
    margin-bottom: 20px;
    list-style-type: none;
  }
  
  .error-list li {
    margin: 5px 0;
  }
  
  .form-content {
    display: flex;
    flex-direction: column;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  .form-group label {
    display: block;
    font-weight: bold;
    margin-bottom: 8px;
  }
  
  .form-group input[type="text"],
  .form-group input[type="email"],
  .form-group input[type="password"],
  .form-group select {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    outline: none;
  }
  
  .checkbox-group label,
  .radio-group label {
    display: inline-block;
    margin-right: 15px;
    font-weight: normal;
  }
  
  .submit-btn {
    background-color: #4a90e2;
    color: white;
    padding: 12px;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
  }
  
  .submit-btn:hover {
    background-color: #357ab8;
  }
  </style>
  