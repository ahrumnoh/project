<!-- eslint-disable vue/valid-template-root -->
<template>
    <div></div>
</template>
<script>
import axios from 'axios';

export default {
    created() {
        axios.get('users')
        .then(response => this.user)
    }
  components: {},
  data() {
    return {
      sampleData: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
