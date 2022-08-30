<!-- eslint-disable vue/valid-template-root -->
<!-- 양방향 연결된 곳:: v-model-->
<template>
<div>
    <select name="" id="" v-model="selectedCity">
        <option value=""></option>
        <option value="02">seoul</option>
        <option value="051">busan</option>
        <option value="064">jeju</option>
    </select>
</div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '02'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
