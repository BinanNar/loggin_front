<template>
    <v-row justify="center">
        <h1>estas logeado {{ nombre }}</h1>
    </v-row>
</template>

<script>


  export default {

    data: () => ({
    //
    nombre:"......",

  }),
    
    methods:{

    }
    ,
    mounted(){
        console.log(this.$route)
        this.nombre = this.$route.query.nombre
        
    }
  }
</script>
