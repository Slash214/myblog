<template>
  <div class="safebox">
    <div class="main fl sb">
      <div class="left">
        <li v-for="i in 10" :key="i">{{ i }}左边内容</li>
      </div>
      <div class="right">右边边内容</div>
    </div>
    <div class="comment">
      <el-input
        class="text"
        type="textarea"
        @blur="onBlur"
        placeholder="输入评论内容"
        v-model="commentKeyword"
        maxlength="300"
        show-word-limit
        @focus="onFocus"
        :rows="5"
      >
      </el-input>
      <div class="btn" v-show="focusflag">
        <el-button type="danger" plain @click="getComment">评论</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      commentKeyword: '',
      focusflag: false
    }
  },
  created () {},
  methods: {
    getComment () {
      console.log(this.commentKeyword)
    },
    onFocus () {
      this.focusflag = true
    },
    onBlur () {
      this.focusflag = false
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
      width: 70%;
      padding: 20px;
      li {
        padding: 20px;
      }
    }
    .right {
      width: 25%;
    }
  }
  .comment {
    width: 70%;
    margin-top: 20px;
    background: #fff;
    padding: 20px;
    .text {
    }
    .btn {
      margin-top: 10px;
      text-align: right;
    }
  }
}
</style>
