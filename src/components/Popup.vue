<template>
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
            <v-form>
                <v-text-field v-model="title"  prepend-icon="mdi-folder" label="Title" ></v-text-field>
                <v-textarea v-model="description" prepend-icon="mdi-pencil" label="Info" ></v-textarea>
                <v-btn @click="submit" color="mx-0 mt-3 success" > Add project </v-btn>
            </v-form>
        </v-card-text>
      </v-card>
    </v-dialog>

</template>

<script>
export default {

    data(){
        return{
            title: '',
            description:'',
        }
    },
    methods:{
        submit(){
            console.log(this.title, this.description)
        }
    }

}
</script>

<style>

</style>