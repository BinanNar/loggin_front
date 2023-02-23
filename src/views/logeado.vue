<template>
<v-container>
    <v-row justify="center">
        <h1>estas logeado {{ nombre }}</h1>
    </v-row>
    <v-row justify="center">
        <v-btn v-on:click="logout()">salirte de microsoft XD</v-btn>
    </v-row>
</v-container>
</template>

<script>


  export default {

    data: () => ({
    //
    nombre:"......",

  }),
    
    methods:{

      logout(){

          window.location.href = "https://login.microsoftonline.com/aeaf81cc-0972-471b-8cda-378007902baf/oauth2/logout?post_logout_redirect_uri=http%3A%2F%2Flocalhost:8000%2Flogout"
      
      }

    }
    ,
    mounted(){
        console.log(this.$route)
        this.nombre = this.$route.query.nombre
        
    }
  }
</script>
