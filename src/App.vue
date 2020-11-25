<template>
  <v-app id="inspire">
      <router-view/>
      <div>    
      
      </div>
  </v-app>
</template>

<script>



  export default {
    name:'App',
    components: {
   
  },
    data: () => ({
     
      links: [
        'About',
        'Messages',
        'Profile',
        'Updates',
      ],
    }),
  }
</script>