<template>
  <div class="app-container">
    {{ equId }}
  </div>
</template>
<script>
export default {
  props: {
    equId: {
      type: Number
    }
  },
  data() {},
  created() {
    // Why need to make a copy of this.$route here?
    // Because if you enter this page and quickly switch tag, may be in the execution of the setTagsViewTitle function, this.$route is no longer pointing to the current page
    // https://github.com/PanJiaChen/vue-element-admin/issues/1221
    this.tempRoute = Object.assign({}, this.$route)
  },
  methods: {}
}

</script>
<style lang="scss" scoped>
</style>
