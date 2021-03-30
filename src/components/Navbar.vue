<template>
   <nav>
    <v-toolbar height="52px" >
      <v-app-bar-nav-icon class="grey--text"  @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text"  > 
          <span class="font-weight-light">Todo</span>
          <span>Ninja</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn depressed class="">Sign Out 
        <!-- <v-icon>exit_to_app</v-icon> -->
      </v-btn>

    </v-toolbar>

    <v-navigation-drawer app  v-model="drawer" >
      <v-list-item  >
        <v-list-item-content height="60px">
          <v-list-item-title class="title grey--text text-uppercase">
            TodoNinja
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
       <v-list-item-group color="red" >
        <v-list-item v-for="link in links" :key="link.text"
                                      router :to="link.route">
          <!-- <v-list-item-icon>
            <v-icon>{{ link.icon }}</v-icon>
          </v-list-item-icon> --> 
      
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
          {icon:'dashboard', text:'Dashboard',route:'/' },
          {icon:'projects', text:'Projects',route:'/projects' },
          {icon:'team', text:'Team',route:'/team' },
        ]
      }
    

  }


  }
    
</script>
