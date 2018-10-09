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
               
                <v-list-tile-title v-html="item.name"></v-list-tile-title>
              <v-list-tile-title v-html="item.button"></v-list-tile-title>
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
            Status: 'Good',
            button:  ' <button @click="changeStatus">Change Status</button>'
},
          { name: 'Serve 2',
          Status: 'Bad',
            button:  ' <button @click="changeStatus">Change Status</button>'
           },
            { name: 'Serve 3',
            Status: 'Terrible',
                        button:  ' <button @click="changeStatus">Change Status</button>'
},
            { name: 'Serve 4',
            Status: 'Nice',
                        button:  ' <button @click="changeStatus">Change Status</button>'
},
            { name: 'Serve 5',
            Status: 'Okay',
                        button:  ' <button @click="changeStatus">Change Status</button>'
}
            ]
}
}

}








</script>




<style scoped>

</style>