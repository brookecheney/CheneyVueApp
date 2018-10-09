<template>
   <v-layout row>
     <v-flex xs6 0sm offset-sm0>
      <v-card>
        <v-list two-line>
          <template v-for="(item) in newList">
            <v-list-tile
              :key="item"
            >
                
              <v-list-tile-content>
                <my-cmp></my-cmp>
                <my-cmp></my-cmp>
                <v-list-tile-title v-html="item.name"></v-list-tile-title>
                <v-list-tile-title v-html="item.Status"></v-list-tile-title>

              </v-list-tile-content>
            </v-list-tile>
         </template>

        </v-list>
      </v-card>
    </v-flex>
  </v-layout>

</template>





 


<script>
export default {
    data: function ()  {
    
    return {
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
}
}

}

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




<style scoped>

</style>