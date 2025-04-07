<template>
    <h1>HomePage</h1>
    <!-- Interpolation is {{  }} double curly braces -->
    <h2>Interpolation</h2>
    <h2>Interpolation {{ 20+20 }}</h2>
    <h2>Interpolation {{ "Ibrahim".length }}</h2>
    <h2>Name : {{ name }}</h2>
    <h2>Email : {{ email }}</h2>
    <h2>FullName : {{ getName() }}</h2>
    <h3>School : {{ getSchool() }}</h3>
</template>

<script>
export default {
    name: 'HomePage',
    data(){
        return {
            email: "abc@gm.com",
            name: "Araf"
        }
    },
    methods:{
        getSchool(){
            return "Green Field School"
        },
        getName(){
            return "Md Ibrahim Khalil"
        }
    }
}
</script>

<style scoped>
h1, h2 {
    color: red;
}
h2 {
    font-size: 50px;
}
</style>
