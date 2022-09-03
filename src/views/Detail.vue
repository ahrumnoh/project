<!-- eslint-disable vue/multi-word-component-names -->
<!-- eslint-disable no-labels -->
<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
       <p>{{ article.id }}</p>
       <p>{{ article.userId }}</p>
       <p>{{ article.title }}</p>
       <p>{{ article.body }}</p>

       <br>
       <el-button @click="goBack">Back</el-button>
    </div>
</template>
<script>
import apiBoard from '@/api/board'
export default {
  components: {},
  data() {
    return {
      article: ''
    }
  },
  mounted() {
    apiBoard.getArticle(this.$route.params.id)
      .then((response) => {
        this.article = response.data
      })
      .catch((e) => {
        console.log(e)
      })
  },
  unmounted() {
  },
  methods: {
    goBack() {
      this.$router.go(-1)
    }
  }
}
</script>
