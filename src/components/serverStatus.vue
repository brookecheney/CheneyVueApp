<template>
<div>
   <v-layout row>
     <v-flex xs2 sm2 offset-sm6>
     <h2>Server Status:  {{ status }} </h2>
     <hr>
     <button @click="changeStatus">Change Status</button>
     
    </v-flex>

  </v-layout>
</div>
  </template>



<script>
export default {
   data: function() {
      return {
        status: 'Critical'
      }
    },
    methods: {
      changeStatus() {
        this.status = 'Normal';
      }
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
  margin-top: 60px;
}
</style>

