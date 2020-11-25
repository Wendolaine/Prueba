<template>   
  <div >   
    <HelloWorld/> 
    <!---------------->
    <!--FOOTER-------->
    <!---------------->
    <v-footer color="#540a3f" >
      <v-row>
        <v-col cols="12">
          <v-card flat title color="#880E4F" class="white--text d-flex" >
            <v-col cols="md-4">
              <v-img 
              src="../assets/N.png"
              max-height="200"
              max-widht="250"
              ></v-img>
            </v-col>

            <!-- Contacto -->
            <v-col cols="md-3" > 
              <h1 class="contact-tit">Contáctanos</h1>
              <hr> <!-- linea divisora -->
              <v-card-text class="sub-contact">
                <v-icon dark>mdi-map-marker</v-icon>
                Ubicación, Concepción
                <v-spacer/>
                <v-icon dark>mdi-phone</v-icon> 
                +56999999911
                <v-spacer/>
                <v-icon dark>mdi-email</v-icon> 
                correo@ejemplo.com
              </v-card-text>
            </v-col>

            <!-- Siguenos -->
            <v-col cols="md-3" >
              <h1 class="contact-tit">Síguenos</h1>
              <hr> <!-- linea divisora -->
              <v-card-text class="sub-contact" > 
                <v-btn class="mx-3" dark icon> 
                  <v-icon size="24px">fab fa-facebook</v-icon> 
                </v-btn>
                <v-btn class="mx-3" dark icon> 
                  <v-icon size="24px">fab fa-youtube</v-icon> 
                </v-btn>
              </v-card-text>
            </v-col>
            
          </v-card>
          
          <v-col >
          <v-card-text class="text-center white--text pa-0 ma-0 " >
            &copy;2020 - <strong>Niufleex</strong>
          </v-card-text>
        </v-col>
        </v-col>
        
        
      </v-row>
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
  },
  data: ()=>({
   
  })
}
</script>

<style>
.contact-tit{
  text-align: center;
  font-family: Palatino Linotype;
}
hr {
color: rgb(212, 159, 159);
width: 80%;
margin-left: 10%;
}
.sub-contact{
  text-align:left ;
  font-family: sans-serif;
  align-content: left;
}



</style>
