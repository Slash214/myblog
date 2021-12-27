<template>
  <div class="safebox">
    <div class="main fl">
      <div class="left">
        <li v-for="i in 10" :key="i">{{ i }}左边内容</li>
      </div>
      <div class="right ml20">右边边内容</div>
    </div>
    <div class="comment">
      <el-input
        class="text"
        type="textarea"
        placeholder="请输入内容"
        v-model="commentKeyword"
        maxlength="300"
        show-word-limit
        :rows="5"
      >
      </el-input>
      <div class="btn fl sb al">
        <el-button type="danger" plain>测试</el-button>
        <el-button type="danger" plain @click="getComment">评论</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      commentKeyword: ''
    }
  },
  created () {},
  methods: {
    getComment () {
      console.log(this.commentKeyword)
    }
  },
  components: {}
}
</script>

<style lang="scss" scoped>
.safebox {
  // padding: 20px;
  padding-bottom: 80px;
  margin-top: 20px;
  .main {
    .left {
      background: #fff;
      // border: 1px solid #ddd;
      width: 1000px;
      padding: 20px;
      li {
        padding: 20px;
      }
    }
  }
  .comment {
    width: 1000px;
    margin-top: 20px;
    background: #fff;
    padding: 20px;
    .btn {
      margin-top: 20px;
    }
  }
}
</style>
