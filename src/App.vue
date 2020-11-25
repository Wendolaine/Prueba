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
      icons:[
        'fab fa-facebook',
        'fab fa-youtube'
      ],
      links: [
        'About',
        'Messages',
        'Profile',
        'Updates',
      ],
    }),
  }
</script>