<template>
  <div class="team">
    <h1 class="subheading grey--text my-5" >Dashboard</h1>
    <v-container class="my-5" >
        <v-card class="pa-3" flat v-for="project in projects" :key="project.title"  >
          <v-layout row wrap :class="`pa-3 project ${project.status}`" >
            <v-flex xs12 sm4 md6 >
              <div :class="`caption  ${project.status}`" >Project title</div>
              <div> {{project.title}} </div>
            </v-flex>

            <v-flex xs6 sm4 md2 >
             <div class="caption" >Person</div>
              <div> {{project.person}} </div>
            </v-flex>

            <v-flex xs6 sm4 md2 >
            <div class="caption" >Due by</div>
              <div> {{project.due}} 1</div>
            </v-flex>

            <v-flex xs2 sm4 md2 >
            <div class="caption" >Status</div>
              <div> {{project.status}} </div>
            </v-flex>

          </v-layout>
          <v-divider></v-divider>
        </v-card>
    </v-container>
  </div>

</template>


<script>


export default {
  name: 'Dashboard',

  data(){
    return{
      projects:[
        {title:'Work on the Frontend vuetify',person:'Aston',due:'31 March 2021',status:'Ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'Reviw my Laravel API projects',person:'Aston',due:'31 March 2021',status:'Ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'Work on Vuex',person:'Me',due:'9 April 2021',status:'Ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'work on Content Management System',person:'Aston',due:'31 April 2021',status:'Ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        }

      ]
    
    }
  }
 
}
</script>


<style scoped >

    .project.complete {
      border-left: 4px solid #3cd12c
    }
    .project.ongoing {
      border-left: 4px solid orange 
    }
    .project.overdue {
      border-left: 4px solid tomato
    }


</style>