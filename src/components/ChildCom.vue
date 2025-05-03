<template>
  <div class="cart">
    <header>
    <slot name="header"></slot>
  </header>
  <content>
    <slot name="main"></slot>
  </content>
  <footer>
    <slot name="footer"><h1>Footer</h1></slot>
  </footer>
  </div>
</template>
<script>
export default {
  name: "ChildCom",
};
</script>
<style scoped>
.cart{
    border: 1px solid red;
    width: 400px;
    text-align: center;
    margin-bottom: 20px;
    border-radius: 5px;
}
</style>
