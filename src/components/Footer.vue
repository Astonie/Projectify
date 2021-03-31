<template>
  <v-footer
    dark
    padless
    class=""
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="link in links"
          :key="link.icon"
          class="mx-4"
          dark
          icon
          router :to="link.route"
        >
          <v-icon size="24px">
            {{ link.icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        All rights reserved @ {{ new Date().getFullYear() }} — <strong>WebSoftAi Inc</strong>
      </v-card-text>
    </v-card>
  </v-footer>

</template>

<script>
export default {
    data(){
        return{
            links:[{icon:'mdi-instagram',route:'/instagram.com'},
            {icon:'mdi-facebook',route:'/facebook.com/astoniemukiwa.7'},
            {icon:'mdi-twitter',route:'/twitter.com'},
            {icon:'mdi-youtube',route:'/youtube.com'}]
        }
    }
}
</script>

<style>

</style>