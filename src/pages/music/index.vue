<template>
  <div class="counter-warp">
    <img src="http://p1.music.126.net/zHc8QgE0TLI1nQnWeft0Yw==/109951163403299614.jpg?param=177y177"
        background-size="cover" />
    <a href="/pages/index/main" class="home">去往首页</a>
  </div>
</template>

<script>
// Use Vuex
// import store from './store'

export default {
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
