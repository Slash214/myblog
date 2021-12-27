<template>
  <div id="app">
    <ahh-header></ahh-header>
    <router-view/>
    <ahh-footer></ahh-footer>
  </div>
</template>

<script>
import AhhHeader from './base/AhhHeader.vue'
import AhhFooter from './base/AhhFooter.vue'
export default {
  components: {
    AhhHeader,
    AhhFooter
  }
}
</script>
<style lang="scss">
</style>
