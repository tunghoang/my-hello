<template>
  <div id="app">
    <my-hello v-for='l in leaders' :name="l" :key="l" 
      @leaderremove="doRemove(l)"></my-hello>
  </div>
</template>

<script>
import MyHello from './components/my-hello';

export default {
  name: 'App',
  data: function() {
    return {
      leaders: ['Steve', 'Trong', 'Bill', 'Obama']
    }
  },
  methods: {
    doRemove: function(name) {
      console.log('do remove');
      console.log(name);
      let index = this.leaders.findIndex((item) => item === name);
      this.leaders.splice(index, 1);
    }
  },
  components: {
    MyHello
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
