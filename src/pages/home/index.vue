<template>
  <div class="counter-warp">
    <card :text="homeText"></card>
    <a href="/pages/index/main" class="home">去往首页</a>
  </div>
</template>

<script>
// Use Vuex
// import store from './store'
import card from '@/components/card'

export default {
  data () {
    return {
      homeText: '还没有想好写啥。。。'
    }
  },

  components: {
    card
  },

  computed: {
    count () {
    //   return store.state.count
    }
  },
  methods: {
    // increment () {
    //   store.commit('increment')
    // },
    // decrement () {
    //   store.commit('decrement')
    // }
  }
}
</script>

<style>
.counter-warp {
  text-align: center;
  margin-top: 20px;
}
.home {
  display: inline-block;
  margin: 100px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
