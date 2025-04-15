<template>
  <h1>HomePage</h1>
  <h3>{{ text }}</h3>
  <div v-html="html1 + html2">
  </div>

</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
      text:"Md Ibrahim",
      html1:"<h1>Md Ibrahim Khalil Ullah</h1>",
      html2:"<h1>Araf Ahmed</h1>",
    }
  }
}
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
