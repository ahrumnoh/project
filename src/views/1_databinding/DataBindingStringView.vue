<!-- eslint-disable vue/valid-template-root -->
<template>
    <div>
        <h1>Hello {{ userName }}</h1>
        <p> {{ message }}</p>
    </div>
</template>
<script>
export default {
  data() {
    return {
      userName: 'World',
      message: 'Welcome Lantern World',
      arr: [],
      obj: {}
    }
  }
}
</script>
<style scoped>
.text-red{
    color:red;
}
</style>
