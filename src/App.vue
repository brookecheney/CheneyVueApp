<template>
  <div id="app">
    <myhead/>
    <myServerStatus/>
    <myServerList/>
    <myfoot/>
  </div>
</template>

<script>
import header from './components/header.vue'
import footer from './components/footer.vue'
import serverList from './components/serverList.vue'
import serverStatus from './components/serverStatus.vue'

export default {
  name: 'app',
  components: {
    'myhead': header,
    'myfoot': footer,
    'myServerList': serverList,
    'myServerStatus': serverStatus
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color:lightpink;
  margin-top: 60px;
}
</style>
