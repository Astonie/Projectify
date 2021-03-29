<template>
  
   <div>
      <v-toolbar>
      <v-toolbar-side-icon  class="grey--text" > <v-btn depressed @click="drawer = !drawer">icon</v-btn> 
      </v-toolbar-side-icon>
      <v-toolbar-title class="text-uppercase grey--text" > 
          <span class="font-weight-light">Todo</span>
          <span>Ninja</span>
         
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn depressed class="">Sign Out 
        <!-- <v-icon>exit_to_app</v-icon> -->
      </v-btn>

    </v-toolbar>

    <v-navigation-drawer app class="success" v-model="drawer" >
          <p>Test</p>
    </v-navigation-drawer>
   </div>
 
</template>

<script>
  export default {
    name: 'Navbar',

  data(){

      return {
        drawer:false
      }
    

  }


  }
    
</script>
