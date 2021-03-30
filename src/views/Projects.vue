<template>
  <div class="team my-5">
    <h1 class="subheading grey--text" >Projects</h1>
    <v-container class="my-5">

   <v-expansion-panels>
    <v-expansion-panel
      v-for="project in myProjects" :key="project.title">

      <v-expansion-panel-header>
        <v-card flat >
          <v-card-text>
            <div> {{project.title}}</div> 
          </v-card-text>
        </v-card>
      </v-expansion-panel-header>

      <v-expansion-panel-content>
          <div class="caption grey--text font-weight-bold">Due by {{project.due}} </div>
        {{project.description}}
      </v-expansion-panel-content>
    </v-expansion-panel>

  </v-expansion-panels>

    
    </v-container>
  </div>
</template>

<script>
export default {
 data(){
    return{
      projects:[
        {title:'Work on the Frontend vuetify',person:'Aston',due:'31 March 2021',status:'complete',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'Reviw my Laravel API projects',person:'Aston',due:'31 March 2021',status:'ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'Work on Vuex',person:'Me',due:'9 April 2021',status:'overdue',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
            {title:'work on Content Management System',person:'Aston',due:'31 April 2021',status:'ongoing',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },
        {title:'Django APIs refactoring',person:'Me',due:'10 May 2021',status:'overdue',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam tenetur impedit at, blanditiis veritatis incidunt commodi veniam esse dolorum, eius provident exercitationem ut laboriosam fuga ad soluta non accusamus molestiae.'
        },

      ]
      
  }
 },
 computed:{
   myProjects(){
     return this.projects.filter(project =>{
       return project.person === 'Me'
     })
   }
 }
}
</script>
