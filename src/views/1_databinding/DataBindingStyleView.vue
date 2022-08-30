<!-- eslint-disable vue/valid-template-root -->
<template>
     <div style="color: red; font-size: 30px">
         Style binding red, font size: 30px
     </div>
     <div :style="style1"> Style binding red, font size: 30px </div>
     <button @click="style1.color= 'blue'"> changing color </button>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: 'green',
        fontSize: '50px'
      }
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
