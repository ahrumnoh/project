<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <el-input type="text" v-model="title"></el-input>
        <el-input type="textarea" rows="10" v-model="body"></el-input>
    </div>

    <br>
    <el-button @click="writeArticle"> store </el-button>
</template>
<script>
import apiBoard from '@/api/board'

export default {
  components: {},
  data() {
    return {
      title: '',
      body: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    writeArticle() {
      if (!this.title || !this.body) {
        this.$message.error('you should write title and body, please')
        return
      }

      apiBoard
        .postArticle(0, this.title, this.body)
        .then((response) => {
          console.log(response)
          this.$router.push({ path: '/' })
        })
        .catch((e) => {
          console.log(e)
          this.$message.error('error occurs during writing')
        })
    }
  }
}
</script>
