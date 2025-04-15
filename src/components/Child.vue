<template>
<h1>This is Child Component</h1>
<h1>Data from Parent Components are "{{ name }}"

    {{ details.name }}
    {{ details.email }}

</h1>
<button v-on:click="functionCall()">Click Me</button>
</template>
<script>
export default {
    name:'ChildComponent',
    props:{
        name:String,
        details:Object,
        functionCall:Function
    }
}
</script>
<style lang="css" scoped>
</style>