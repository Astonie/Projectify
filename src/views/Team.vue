<template>
  <div class="team">
    <h1 class="subheading grey--text my-5" >Team</h1>
    <v-container>

        <v-layout row wrap>
          <v-flex xs12 sm6 md4 v-for="person in team" :key="person.name" >
              <v-card flat class="text-xs-center ma-3" >
                <v-responsive pt-4 >
                  <v-avatar size="100">
                    <img :src="person.avatar" alt="">
                  </v-avatar>
                </v-responsive>
                <v-card-text>
                  <div class="subheading text-xs-center"> {{person.name}} </div>
                  <div class="gray--text"> {{person.role}} </div>
                </v-card-text>
                <v-card-actions>
                  <v-btn small grey >
                    Message
                  </v-btn>
                </v-card-actions>

              </v-card>
          </v-flex>
        </v-layout>

    </v-container>
  </div>
</template>

<script>
export default {
    data(){
      return{
        team:[
          {name:'Aston Muk',role:'UI/UX designer',avatar:'/avatar-1.jpg' },
          {name:'Raymond',role:'Backend Developer',avatar:'/avatar-2.jpg' },
          {name:'Fumban Banda',role:'Django Developer',avatar:'/avatar-3.jpg' },
          {name:'Gerson Aziba',role:'FullStack Developer',avatar:'/avatar-4.jpg' },
          {name:'Khumbo',role:'Web Designer',avatar:'/avatar-5.jpg' },
        ]
      }
    }
}
</script>