<template>
  <div class="counter-warp">
    <p>Vuex counter：{{ count }}</p>
    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>

    <a href="/pages/index/main" class="home">去往首页</a>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
// Use Vuex
import store from './store';

export default {
  computed: {
    count() {
      return store.state.count;
    },
  },
  methods: {
    increment() {
      store.commit('increment');
    },
    decrement() {
      store.commit('decrement');
    },
    handleClick() {
      console.log('click me!!!!');
    },
  },
};
</script>

<style lang="scss">
.counter-warp {
  text-align: center;
  margin-top: 100px;
  background-color: red;
}
.home {
  display: inline-block;
  margin: 100px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
