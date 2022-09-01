<template>
  <hi> {{title}}</hi>
  <el-table :data="articles" style="width: 100%">
    <el-table-column prop="id" label="id" width="80"></el-table-column>
    <el-table-column prop="userId" label="userId" width="120"></el-table-column>
    <el-table-column prop="title" label="title"></el-table-column>

  </el-table>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import apiBoard from '@/api/board'

export default {
  data() {
    return {
      title: 'hi, ahahaha',
      articles: null
    }
  },
  mounted() {
    apiBoard.getArticles(0)
      .then((response) => {
        console.log('getArticle', response)
        this.articles = response.data
      })
      .catch((e) => {
        console.log(e)
      })/*  <--- error function을 이용한  */
  },
  name: 'HomeView',
  components: {
    HelloWorld

  }
}
</script>
