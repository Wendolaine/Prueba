<template>

  <v-container >
      <!---------------->
      <!--barra de nav-->
      <!---------------->
      <v-row wrap >
      <v-app-bar app color="#5a0c52" flat >
        <v-col cols="12">
        <v-avatar class="mr-10" color="grey darken-1" size="32"></v-avatar>        
        
        <v-btn  color="#5a0c52" class="white--text left" >
          <router-link to="/About" class="white--text">About</router-link></v-btn>
        <v-btn  color="#5a0c52"  >
          <router-link class="white--text " to="/login">Login</router-link></v-btn>

        <!--<v-responsive max-width="230">
          <v-text-field dense flat hide-details rounded solo-inverted></v-text-field>
        </v-responsive>-->
        </v-col>
      </v-app-bar>      

    
      <!------------>
      <!--carrusel-->
      <!------------>
      <v-col cols="12">
        <v-carousel show-arrows-on-hover >
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
      </v-col>

      <!-------------------->
      <!--tarjetas de publ-->
      <!-------------------->
      <v-col cols="4">
        <v-card>
          <v-img src="https://picsum.photos/510/300?random"></v-img>
          <v-card-tittle><h2>Titulo</h2></v-card-tittle>
          <v-card-text><p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat, doloremque saepe fugit eius iure voluptatem eum quos non libero ad blanditiis vel voluptate aperiam nemo esse.
              Itaque consequatur recusandae maxime!</p></v-card-text>
          <v-card-actions><v-btn flat color="info">Leer más</v-btn></v-card-actions>
        </v-card>
      </v-col>

      <v-col cols="4">
        <v-card>
          <v-img src="https://picsum.photos/510/300?random"></v-img>
          <v-card-tittle><h2>Otro titulo</h2></v-card-tittle>
          <v-card-text><p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat, doloremque saepe fugit eius iure voluptatem eum quos non libero ad blanditiis vel voluptate aperiam nemo esse.
              Itaque consequatur recusandae maxime!</p></v-card-text>
          <v-card-actions><v-btn color="info" flat>Leer más</v-btn></v-card-actions>
        </v-card>
      </v-col>

      <v-col cols="4">
        <v-card>
          <v-img src="https://picsum.photos/510/300?random"></v-img>
          <v-card-tittle><h2>Ultimo titulo</h2></v-card-tittle>
          <v-card-text><p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Fugiat, doloremque saepe fugit eius iure voluptatem eum quos non libero ad blanditiis vel voluptate aperiam nemo esse.
              Itaque consequatur recusandae maxime!</p></v-card-text>
          <v-card-actions><v-btn color="info" flat>Leer más</v-btn></v-card-actions>
        </v-card>
      </v-col>


      <!-------------------->
      <!--antes de footer--->
      <!-------------------->       
      <v-col cols="6">   
          <v-card  class="card-prefoot">           
                <div class="text-sm-center card-texto">Únete a NIUFLEEX y aprovecha 
                  los beneficios que ofrecemos</div>           
          </v-card>
      </v-col>
          
      <v-col cols="3">   
        <v-card color="#FCE4EC" class="card-prefoot"> 
          <div class="icon-prefoot">
            <v-icon x-large color="#5a0c52">mdi-thumbs-up-down</v-icon>            
          </div>
          <div class="text-sm-center card-texto">Crea tu propio contenido</div>  
        </v-card>
      </v-col>

      <v-col cols="3" >   
        <v-card color="#FCE4EC" class="card-prefoot">  
          <div class="icon-prefoot">
            <v-icon  x-large color="#5a0c52" >fa-file-alt</v-icon>            
          </div>
          <div class="card-texto">Visualiza contenido exclusivo</div>            
        </v-card>
      </v-col>

    </v-row>

  </v-container>
  
</template>



<script>
import Vue from 'vue'
import Vuetify from 'vuetify'
Vue.use(Vuetify, {
  iconfont: 'mdi' // 'md' || 'mdi' || 'fa' || 'fa4'
})
  export default {
    
    name: 'HelloWorld',

    //IMAGENES DEL CARRUSEL
    data () {
      return {
        items: [
          {src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'},
          {src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'},
          {src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'},
          {src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'}
        ]
      }
    },
  }  


</script>

<style>
/* texto de card */
.card-texto{
  color:#5a0c52;
  font-family: Segoe IU;
  font-weight:bold;
  text-align: center;
  font-size: 40px;
  
}

.card-prefoot{
  padding-top: 80px;
  height: 20rem;
}

.icon-prefoot{
  display: flex;
  flex-flow: column wrap;
}
</style>