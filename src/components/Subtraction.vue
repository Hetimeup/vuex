<template>
  <div>
    <!-- <h3>当前 Count 值为：{{ count }}</h3> -->
    <h3>{{ showNum }}</h3>
    <button @click="btnHandler1">-1</button>
    <button @click="btnHandler2">-N</button>
    <button @click="subAsync">-1 Async</button>
    <button @click="subNAsync(5)">-N Async</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'
export default {
  data() {
    return {}
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNum'])
  },
  methods: {
    ...mapMutations(['sub', 'subN']),
    ...mapActions(['subAsync', 'subNAsync']),
    btnHandler1() {
      this.sub()
    },
    btnHandler2() {
      this.subN(3)
    }
  }
}
</script>

<style>
</style>