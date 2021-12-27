<template>
  <div class="index">卡片</div>
</template>

<script>
export default {
  props: {
    obj: {
      type: Object,
      default: () => {}
    }
  },
  methods: {
    lookDetail (e) {
      //   this.$emit(e)
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
