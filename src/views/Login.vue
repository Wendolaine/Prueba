<template>
  <v-container id="signinup-form" class="fill-height" >
    
    <v-row align="center" justify="center" no-gutters>
      <v-col cols="12" sm="8" md="8" class="">
        <v-card class="evelation-15 card">
          <v-window v-model="step">
            <!----------->
            <!--Ingreso-->
            <!----------->
            <v-window-item :value="1">
              <v-row class="">
                <v-col cols="12" md="8" class="pt-0 pb-10">
                  <v-card-text>
                    <v-form class="signup-form-form" @submit.prevent="signin">
                        <h1 class="text-center display-1 mb-10" :class="`${bgColor}--text`">
                            Acceso
                        </h1>
                        <!--nombre usuario-->
                        <v-text-field
                            id="nomusuario"
                            v-model="login"
                            label="Nombre usuario"
                            name="nomusuario"
                            append-icon="fa-user"
                            type="text"
                            color="#880E4F"/>
                    
                        <!--Contraseña-->
                        <v-text-field
                            id="password"
                            v-model="password"
                            label="Contraseña"
                            name="Password"                       
                            append-icon="mdi-lock"
                            type="password"
                            color="#880E4F"/>
                      
                        <!--Checkbox-->
                        <v-checkbox
                           color="#880E4F"
                           label="Recuerdame">
                        </v-checkbox>            

                        <!--Boton iniciar sesion-->
                        <div class="text-center mt-6">
                            <v-btn rounded type="submit" large color="#880E4F" dark 
                            >Iniciar sesión</v-btn>
                        </div>
                        
                        <!-- olvida contraseña-->
                        <div class="text-center">
                            <a
                                href="#"
                                class="pa-5 overline no-text-decoration"
                                :class="`${bgColor}--text`"
                                @click="step = 3"
                                >
                                He olvidado mi contraseña
                            </a>
                        </div>
                      
                    </v-form>
                  </v-card-text>
                </v-col>

                <!------------------->
                <!--tarjeta derecha-->
                <!------------------->
                <v-col
                  cols="12"
                  md="4"
                  class="darken-2 vcenter "
                  
                >
                  <div >
                    <v-card-text  :class="`${fgColor}--text` ">
                      <h1 class="text-center headline mb-3">¡HOLA!</h1>
                      <h5 class="text-center overline mb-2">¿No estás registrado en NIUFLEEX? </h5>
                    </v-card-text>
                    <!-- Boton registro -->
                    <div class="text-center mb-2">
                      <v-btn rounded dark @click="step = 2">Registrarse</v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>

            <!------------>
            <!--Registro-->
            <!------------>
            <v-window-item :value="2">
              <v-row class="fill-height">
                <v-col
                  cols="12"
                  md="4"
                  class=" vcenter primary"
                 
                >
                  <div>
                    <v-card-text :class="`${fgColor}--text`">
                      <h1 class="text-center headline mb-3">¿Ya eres usuario de NIUFLEEX?</h1>
                      <h5 class="text-center overline mb-3">Ingresa a nuestro sitio</h5>
                    </v-card-text>
                    <!-- Boton -->
                    <div class="text-center mb-6">
                      <v-btn rounded dark @click="step = 1">Iniciar sesión</v-btn>
                    </div>
                  </div>
                </v-col>
                <!-- Head -->
                <v-col cols="12" md="8" class=" pt-6 pb-6">
                  <v-card-text>
                    <h1
                      class="text-center display-1 mb-10"
                      :class="`${bgColor}--text`"
                    >
                      Crear una cuenta
                    </h1>

                    <!-- Formulario -->
                    <v-form class="signup-form-form" @submit.prevent="signup">
                      <v-text-field
                        id="nomusuario"
                        v-model="nomusuario"
                        label="Nombre usuario"
                        name="nomusuario"
                        append-icon="fa-user"
                        type="text"
                      />
                      <v-text-field
                        id="email"
                        v-model="email"
                        label="E-mail"
                        name="email"
                        append-icon="mdi-email"
                        type="email"
                      />
                      <v-text-field
                        id="password"
                        v-model="password"
                        label="Contraseña"
                        name="password"
                        append-icon="mdi-lock"
                        type="password"
                      />
                      <v-checkbox
                        color="#880E4F"
                        label="Acepto los términos y condiciones"
                      >                          
                      </v-checkbox>

                      <div class="text-center mt-6">
                        <v-btn rounded type="submit" large color="#880E4F" dark>
                          Registrarse</v-btn
                        >
                      </div>
                      
                    </v-form>
                  </v-card-text>
                </v-col>
              </v-row>
            </v-window-item>

            <!--PW Rest-->
            <v-window-item :value="3">
              <v-row class="fill-height">
                <v-col
                  cols="12"
                  md="4"
                  class="darken-2 vcenter"
                 
                >
                  <div>
                    <v-card-text :class="`${fgColor}--text`">
                      <h1 class="text-center headline mb-3">¿Ya recordaste?</h1>
                      <h5 class="text-center overline mb-3">No te preocupes, aquí puedes ingresar</h5>
                    </v-card-text>
                    <div class="text-center mb-6">
                      <v-btn rounded color="#880E4F" dark @click="step = 1">Iniciar sesión</v-btn>
                    </div>
                  </div>
                </v-col>

                <v-col cols="12" md="8" class="pt-6 pb-6">
                  <v-card-text>
                    <v-form class="signup-form-form">
                      <h1
                        class="text-center display-1 mb-10"
                        :class="`${bgColor}--text`"
                      >
                        Olvidé mi contraseña
                      </h1>
                      <v-text-field
                        id="login"
                        v-model="login"
                        label="nomusuario / eMail"
                        name="login"
                        append-icon="mdi-person /mdi-email"
                        type="text"
                        :color="bgColor"
                        class="v-input__icon--double"
                      />
                      <div class="text-center mt-6">
                        <v-btn rounded large color="#880E4F" dark
                          >Reestablecer contraseña</v-btn
                        >
                      </div>
                    </v-form>
                  </v-card-text>
                </v-col>
              </v-row>
            </v-window-item>
          </v-window>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  name: 'Login',
  components: {
   
  },
  props: {
    source: {
      type: String,
      default: ''
    },
    
    fgColor: {
      type: String,
      default: 'white'
    }
 
  },
  async fetch({ store, error }, user) {
    try {
      await store.dispatch('users/signupUser', user)
    } catch (e) {
      error({
        statusCode: 503,
        message: 'No se pudo registrar al usuario. Por favor, intente de nuevo.'
      })
    }
  },
  data: () => ({
    step: 1,
    nomusuario: '',
    email: '',
    password: '',
    login: '',
    snackbarType: 'success',
    snackbarMessage: '',
    snackbar: false
  }),
  methods: {
    signup() {
      this.$auth
        .signup({
          data: {
            user: {
              nomusuario: this.nomusuario,
              email: this.email,
              password: this.password
            }
          }
        })
        .catch((e) => {
          this.error = e + ''
        })
    },
    async signin() {
      try {
        const response = await this.$auth.loginWith('local', {
          data: {
            login: this.login,
            password: this.password
          }
        })
        this.snackbarType = response.data.type
        this.snackbarMessage = response.data.message
        this.snackbar = true
      } catch (err) {
        this.snackbarType = 'error'
        this.snackbarMessage = 'Error signing you in'
        this.snackbar = true
      }
    }
  }
}
</script>

<style scoped lang="scss">
.v-input__icon--double .v-input__icon {
  margin-left: -4.25rem !important;
}
a.no-text-decoration {
  text-decoration: none;
}
#signinup-form {
  max-width: 150rem;
  
}
.signup-form-form {
  max-width: 23rem;
  margin: 0 auto; 
  
}
.card {
  overflow: hidden;
  height: 750px; //largo

}
.vcenter {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-bottom:100%; //largo fondo con card
  background-image: url('../assets/colores.jpg');
  
}

</style>