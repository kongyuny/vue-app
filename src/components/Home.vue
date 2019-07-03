<template>
  <div class="hello">
    <h2>Home</h2>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: '大标题'
    }
  },
  computed: {
    username () {
      // 我们很快就会看到 `params` 是什么
      return this.$route.params.username
    }
  },
  methods: {
    goBack () {
      window.history.length > 1
        ? this.$router.go(-1)
        : this.$router.push('/')
    }
  }
}
</script>
<style scoped>
</style>
