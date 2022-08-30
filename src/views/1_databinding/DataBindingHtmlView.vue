<!-- eslint-disable vue/valid-template-root -->
<template>
<div>
  <div>{{ htmlString }}</div>
  <div v-html="htmlString" />
</div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      htmlString: '<p style="color:red;">red color texts</p>'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
