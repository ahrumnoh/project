<template>
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
  mounted() {
    apiBoard.getArticle(1)
      .then(function (response) {
        console.log('getArticle', response)
      })
      .catch(function (e) {
        console.log(e)
      })

    apiBoard.getArticles(0)
      .then(function (response) {
        console.log('getArticles', response)
      })
      .catch(function (e) {
        console.log(e)
      })

    apiBoard.postArticle(0)
      .then(function(response) {
        console.log('postArticle', response)
      })
      .catch(function (e) {
        console.log(e)
      })
  },
  name: 'HomeView',
  components: {
    HelloWorld

  }
}
</script>
