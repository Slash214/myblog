<template>
  <div class="safebox fl sb">
    <div class="left">
      <div class=""></div>
      <!-- <div class="list " infinite-scroll-disabled="disabled" v-infinite-scroll="load" style="overflow: auto"> -->
        <div class="card list-item" v-for="(i,index) in 18" :key="index" @click="lookblog(i)">
          <div class="title">{{i}}</div>
          <div class="author fl al">
            <span class="pr10">Author</span>
            <span class="pr10">2021-12-23</span>
            <div>
              <el-link class="mr10" type="primary" v-for="i in 5" :key="i"
                >#主要链接</el-link
              >
            </div>
          </div>
          <div class="content">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
          </div>
        </div>
      <!-- </div> -->
    </div>
    <div class="right">
      <div class="info fl al">
        <el-avatar :size="60" :src="avatar"></el-avatar>
        <div class="fd ml10">
          <span>大羊</span>
          <span>不务正业的程序员</span>
        </div>
      </div>
      <div class="total_tag">
        <el-tag class="tags" v-for="i in tag" :key="i">{{ i }}</el-tag>
      </div>
    </div>
  </div>
</template>

<script>
import { avatar } from '@/common/contast.js'
export default {
  name: 'Home',
  data () {
    return {
      avatar: '',
      list: [],
      count: 0,
      tag: ['css', 'JavaScript', 'Node', 'vue', 'Linux', 'Java', 'Python']
    }
  },
  created () {
    this.avatar = avatar
  },
  methods: {
    lookblog (e) {
      console.log('查看详情')
      this.$router.push(`/article/${e}`)
    },
    load () {
      this.count += 2
    },
    pushList () {
      for (let i = 0; i < 500000; i++) {
        this.list.push(i)
        if (this.list.length === 20) break
      }
    }
  },
  components: {}
}
</script>

<style lang="scss" scoped>
@import '@/style/mixin.scss';
.safebox {
  margin-top: 20px;
  position: relative;
  .left {
    width: 70%;
    .card {
      padding: 20px;
      box-shadow: 0 0 10px 2px #bdbdbd;
      border-radius: 6px;
      background: #fff;
      text-align: justify;
      margin-bottom: 20px;
      position: relative;
      .title {
        font-size: $font-18;
        color: #444;
      }
      .author {
        margin: 10px 0;
      }
      .content {
        @include text_hidden(4);
      }
    }
  }
  .right {
    width: 25%;
    .info {
      width: 100%;
      box-sizing: border-box;
      padding: 20px;
      background: #fff;
    }
    .total_tag {
      margin-top: 20px;
      background: #fff;
      padding: 20px 20px 10px 20px;
      .tags {
        margin-right: 20px;
        margin-bottom: 10px;
      }
    }
  }
}
</style>
