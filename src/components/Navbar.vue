<template>
   <nav>
    <v-toolbar height="52px" >
      <v-app-bar-nav-icon class="grey--text"  @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text"  > 
          <span class="font-weight-light">Todo</span>
          <span>Ninja</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn depressed right class="right">Sign Out 
        <v-icon right >mdi-exit-to-app</v-icon>
      </v-btn>

    </v-toolbar>

    <v-navigation-drawer hide-overlay app class="primary" v-model="drawer" >
      <v-layout column wrap class="align-center" >
        <v-avatar class="ma-4" size="100" >
          <img src="/avatar-1.jpg" alt="">
        </v-avatar>
        <div class="white--text" > Aston Muk </div>
      </v-layout>
      <v-list-item  >
        <v-list-item-content height="60px">
          <v-list-item-title class="title grey--text text-uppercase">
            TodoNinja
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
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
  export default {
    name: 'Navbar',

  data(){

      return {
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
