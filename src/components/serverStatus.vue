<template>
<div id="app">
  
    
       <my-cmp></my-cmp>

  </div>
  </template>

 


<script>
Vue.component('my-cmp',    {
  data: function() {
    return data;
  },
  template: '<p>Server Status: {{ status }} (<button@click="changeStatus">Change</button>)</p>',
  methods: {
    changeStatus: function() {
      this.status = 'Normal' ;
    }
  }
});
</script>





<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

