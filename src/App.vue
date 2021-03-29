<template>
  <div id="app">
    <div id="nav">
      <!-- <v-app class="grey lighten-4">
              <Navbar/>
           </v-app>  -->
          <Navbar/>
          <router-view/>
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->

    </div>
   
  </div>
</template>
<script>
import Navbar from './components/Navbar'

export default {
  components:{
    Navbar, 
  },
    data(){
      return {

      }
    }

}
</script>