<template>
  <v-app class="grey lighten-4">
    <Navbar/>
    <v-main class="mx-4 mb-4" >
      <router-view></router-view>
    </v-main>
  <div class="grey" >
    <Footer/>
  </div>
      
   
  </v-app>
</template>
<script>
import Navbar from './components/Navbar'
import Footer from './components/Footer'

export default {
  components:{
    Navbar, Footer,
  },
    data(){
      return {

      }
    }

}
</script>