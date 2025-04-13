<template>
  <h1>HomePage</h1>
  <input type="text" placeholder="Enter your inputs" v-model="data">
  <h1>{{data}}</h1>
    <h1>Login Details</h1>
  <input type="email" value="email" v-model="email">
  <input type="password" value="email" v-model="password">
  <button v-on:click="clicked()">Log in</button>
  <h2>{{ userStatus }}</h2>

  <h1>Languages</h1>
  <label for="PHP">PHP</label>
  <input type="checkbox" value="PHP" v-model="Languages" id="PHP">
  <label for="JAVA">JAVA</label>
  <input type="checkbox" value="JAVA" v-model="Languages" id="JAVA">
  <label for="NEXTJS">NEXTJS</label>
  <input type="checkbox" value="NEXTJS" v-model="Languages" id="NEXTJS">
  <label for="JS">JS</label>
  <input type="checkbox" value="JS" v-model="Languages" id="JS">
  <label for="LARAVEL">LARAVEL</label>
  <input type="checkbox" value="LARAVEL" v-model="Languages" id="LARAVEL">
  <label for="VUEJS">VUEJS</label>
  <input type="checkbox" value="VUEJS" v-model="Languages" id="VUEJS">
  <h1>{{ Languages }}</h1>


  <h1>Radio - WhoAmI</h1>

  <label for="Student">Student</label>
  <input type="radio" name="who" value="Student" v-model="who" id="Student">
  <label for="Developer">Developer</label>
  <input type="radio" name="who" value="Developer" v-model="who" id="Developer">
  <label for="Doctor">Doctor</label>
  <input type="radio" name="who" value="Doctor" v-model="who" id="Doctor">
  <label for="Engineer">Engineer</label>
  <input type="radio" name="who" value="Engineer" v-model="who" id="Engineer">
  <label for="Teacher">Teacher</label>
  <input type="radio" name="who" value="Teacher" v-model="who" id="Teacher">
  <h1>I am a:{{ who }}</h1>
</template>

<script>
export default {
  name: "HomePage",
  data(){
    return{
        email:null,
        password:null,
        userStatus:0,
        Languages:[],
        who:null,
    }
  },
  methods: {
    clicked(){
        this.userStatus = this.email+" "+this.password;
        return this.userStatus
    }
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
