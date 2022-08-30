<!-- eslint-disable vue/valid-template-root -->
<template>
    <!-- <div>
        <input type="search" name="" id="" @keyup="checkEnter($event)" v-model="searchText">
        <button @click="doSearch"> Search </button>
    </div> -->
    <div>
        <input type="search" name="" id="" @keyup.enter="doSearch" v-model="searchText">
        <button @click="doSearch"> Search </button> <!-- the same function above-->
        <!-- <button type="submit" @click.prevent="doSearch"></button> -->
    </div>
</template>
<script>
// .enter
// .tab
// .delete
// .esc
// .space
// .up
// .down
// .left
// .right
// .stop - event.stopPropagation()
// .prevent - event.preventDefault()
export default {
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
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      // event.stop.propagation();
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>
