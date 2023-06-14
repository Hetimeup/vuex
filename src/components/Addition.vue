<template>
  <div>
    <!-- <h3>当前 Count 值为：{{ $store.state.count }}</h3> -->
    <h3>{{ $store.getters.showNum }}</h3>
    <button @click="btnhandler1">+1</button>
    <button @click="btnhandler2">+N</button>
    <button @click="btnhandler3">+1 Async</button>
    <button @click="btnhandler4">+N Async</button>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    btnhandler1() {
      this.$store.commit('add')
    },
    btnhandler2() {
      this.$store.commit('addN', 3)
    },
    btnhandler3() {
      this.$store.dispatch('addAsync')
    },
    btnhandler4() {
      this.$store.dispatch('addNAsync', 5)
    }
  }
}
</script>

<style>
</style>