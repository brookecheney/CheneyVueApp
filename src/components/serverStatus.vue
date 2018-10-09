<template>
<div>
   <v-layout row>
     <v-flex xs2 sm2 offset-sm6>
     <h2>Server Status:  {{ status }} </h2>
     <hr>
     <button @click="changeStatus">Change Status</button>
      <template v-for="(item) in newList">
            <v-list-tile
              :key="item"
            >
                
              <v-list-tile-content>
               
                <v-list-tile-title v-html="item.name">
                   <button @click="changeStatus">Change Status</button>
                </v-list-tile-title>

                <v-list-tile-title v-html="item.status">
                   <button @click="changeStatus">Change Status</button>
                </v-list-tile-title>

              </v-list-tile-content>
            </v-list-tile>
         </template>
     
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
            newList: [
            { name: 'Serve 1',
            Status: 'Good'},
            { name: 'Serve 2',
            Status: 'Bad'},
            { name: 'Serve 3',
            Status: 'Terrible'},
            { name: 'Serve 4',
            Status: 'Nice'},
            { name: 'Serve 5',
            Status: 'Okay'}
            ]    


      
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

