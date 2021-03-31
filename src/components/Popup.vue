<template>
 <div>
    
     <v-dialog
      width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="success"
          dark
          v-bind="attrs"
          v-on="on"
        >
         Add new project
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="headline grey lighten-2">
          Add a new project
        </v-card-title>

        <v-card-text>
            <v-form ref="form">
                <v-text-field  v-model="title"  prepend-icon="mdi-folder" label="Title" :rules="inputRules" ></v-text-field>
                <v-textarea v-model="description" prepend-icon="mdi-pencil" label="Info" :rules="inputRules"></v-textarea>


        <v-row >
            <v-col cols="12" sm="6" md="4">
            <v-menu
                :close-on-content-click="true" nudge-right="40" transition="scale-transition" offset-y min-width="auto"
            >
                <template v-slot:activator="{ on, attrs }">
                    <v-text-field :rules="inputRules" v-model="due" label="project due date" prepend-icon="mdi-calendar"
                        readonly v-bind="attrs" v-on="on">
                    </v-text-field>
                </template>
                    <v-date-picker v-model="due" @input="menu = false"></v-date-picker>
            </v-menu>
            </v-col>
            <v-spacer></v-spacer>
        </v-row>
        

                <v-spacer></v-spacer>
                <v-btn @click="submit" color="mx-0 mt-3 success" > Add project </v-btn>
            </v-form>
        </v-card-text>
      </v-card>
    </v-dialog>
 </div>

</template>

<script>
export default {

    data(){
        return{
            title: '',
            description:'',
            due:null, 
            inputRules:[ v => v.length >=3 || 'The minimum length is 3'   ]
        }
    },
    methods:{
        submit(){
            if(this.$refs.form.validate()){
                console.log(this.title, this.description, this.due)
                
            }
        }
    }

}
</script>

<style>

</style>