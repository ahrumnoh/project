<!-- eslint-disable vue/valid-template-root -->
<!-- 양방향 호환 -->
<template>
<div>
    <div>
        <input type="radio" name="" id="html" value="HTML" v-model="favouriteLang" />
        <label for="html">HTML</label>
    </div>
    <div>
        <input type="radio" name="" id="css" value="CSS" v-model="favouriteLang" />
        <label for="css">CSS</label>
    </div>
    <div>
        <input type="radio" name="" id="js" value="JS" v-model="favouriteLang" />
        <label for="js">Java Script</label>
    </div>
    <div>🚀 chosen region: {{ favouriteLang }}</div>

</div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      favouriteLang: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
