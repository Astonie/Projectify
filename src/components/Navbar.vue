<template>
   <nav>
     
    <v-toolbar height="52px" >
      <v-app-bar-nav-icon class="grey--text"  @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text"  > 
          <span class="font-weight-light">Todo</span>
          <span>Ninja</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-menu offset-y>

      <template v-slot:activator="{ on: menu, attrs }">
        <v-btn grey depressed v-bind="attrs" v-on="{ ...menu }">
              Menu
        </v-btn>   
      </template>

      <v-list>
        <v-list-item
          router :to="link.route"
          v-for="(link, index) in links"
          :key="index"
        >
          <v-list-item-title>{{ link.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

      <v-btn depressed right class="right">Sign Out 
        <v-icon right >mdi-exit-to-app</v-icon>
      </v-btn>

    </v-toolbar>

    <v-navigation-drawer hide-overlay app class="primary" v-model="drawer" >
      <v-layout column wrap class="align-center" >
        <v-flex>
          <v-avatar class="ma-4" size="100" >
          <img src="/avatar-1.jpg" alt="">
        </v-avatar>
        <div class="white--text" > Aston Muk </div>
        </v-flex>
        <v-flex class="mt-4 mb-3" >
          <Popup/>
        </v-flex>
      </v-layout>
    
      

      <v-divider></v-divider>

      <v-list dense nav class="mt-4 mb-3" >
       <v-list-item-group class="white--text" >
        <v-list-item v-for="link in links" :key="link.text"
                                      router :to="link.route">
          <v-list-item-icon>
            <v-icon>{{ link.icon }}</v-icon>
          </v-list-item-icon> 
      
          <v-list-item-title>
           {{ link.text }}
          </v-list-item-title>
      
        </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  
   </nav>
 
</template>

<script>
  import Popup from './Popup'
  export default {
    name: 'Navbar',
    components:{
      Popup,
    },

  data(){

      return {
        alert:true,
        drawer:false,
        links: [
          {icon:'mdi-view-dashboard', text:'Dashboard',route:'/' },
          {icon:'mdi-folder', text:'My Projects',route:'/projects' },
          {icon:'mdi-account-group', text:'Team',route:'/team' },
        ]
      }
    

  }


  }
    
</script>
