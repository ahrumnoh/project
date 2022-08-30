<!-- eslint-disable vue/valid-template-root -->
<!-- 사용자가 바꾸길 바라지 않으면.. value아이디 속성에 단발형 바인딩이 됨-->
<!-- 조회 기능 -->
<template>
<div>
    <input type="text" name="" id="" v-bind:value="userId" readonly/>
    <input type="text" name="" id="" :value="userId" readonly/>
    <br>
    <img :src ="imgSrc" alt ="" style="width:1000px; height:auto;">
    <br>
    <input type="search" name="" id="" v-model="txt1">
    <button :disabled="txt1 === ''"> Search</button>
</div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'helloworld',
      imgSrc: 'https://s4.scoopwhoop.com/anj/sw/5d2b4793-2a3b-44f9-8411-c77342e5f88f.jpg',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
