<template>
  <header class="headers">
    <div class="safebox fl al">
      <div class="logo">
        <span>大羊博客</span>
      </div>
      <ul class="item fl">
        <router-link tag="li" to="/about">关于</router-link>
        <router-link tag="li" to="/project">项目成品</router-link>
        <router-link tag="li" to="/share">工具</router-link>
        <router-link tag="li" to="/">首页</router-link>
      </ul>
    </div>
  </header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '@/style/mixin.scss';
.headers {
  width: 100%;
  height: 80px;
  background: #fff;
  .safebox {

    height: 80px;
    .logo {
        width: 100px;
    }
    .item {
        cursor: pointer;
        flex: 1;
        flex-direction: row-reverse;
        li {
            font-size: $font-16;
            font-weight: 550;
            padding: 20px;
        }
    }
  }
}
</style>
