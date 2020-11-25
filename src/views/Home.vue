<template>   
  <div >   
    <HelloWorld/> 
    <!---------------->
    <!--FOOTER-------->
    <!---------------->
    <v-footer color="#540a3f" >
      <v-card flat title color="#880E4F" class="white--text text-xs-center flex" >
        <v-card-text class="text-right" >
          <v-btn v-for="icon in icons" :key="icon" class="mx-3 " dark icon>
            <v-icon size="24px" >{{icon}}</v-icon>
            </v-btn>
        </v-card-text>
       
        <v-card-text class="white--text text-center" >
          shopinfdsf
        </v-card-text>

        <v-card-text class="text-center white--text " >
          &copy;2020 - <strong>Niufleex</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </div>
  
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
