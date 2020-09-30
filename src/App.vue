<template>
  <div class="body">
    <div id="header" class="container-fluid">
      <!-- Top bar -->
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="row" id="fixed-top-colapse">
          <div class="col-6" id="logo-area">
            <!-- Company Icon-->
            <img id="logo" src="/custompages/images/logo.png" />
          </div>
        </div>

        <div class="col-md-8">
          <div class="row">
            <div class="col-lg-10">
              <div class="collapse navbar-collapse" id="navbarToggler">
                <ul class="navbar-nav mt-2 mt-lg-0 col-md-12">
                  <div id="itemsNavBar" class="col-sm-4">
                    <li class="nav-item">
                      <a class="nav-link" href="https://pikinglish.com"
                        >SITIO WEBcommit3</a
                      >
                    </li>
                  </div>
                  <!-- Vertical line -->
                  <div class="vertical-line"></div>
                  <div id="itemsNavBar" class="col-sm-4">
                    <li class="nav-item">
                      <a
                        class="nav-link"
                        href="https://classroom.pikinglish.com/"
                        >INGRESAR</a
                      >
                    </li>
                  </div>
                </ul>
              </div>
            </div>
            <!-- Social media icons -->
            <div class="col-lg-2 row" id="iconoSocial">
              <div class="col-xs-3">
                <a href="https://www.facebook.com/Pikinglishcolombia/">
                  <i class="fa fa-facebook"></i>
                </a>
              </div>
              <div class="col-xs-3">
                <a href="https://wa.me/message/3M3QMM5B73FHJ1">
                  <i class="fa fa-whatsapp"></i>
                </a>
              </div>

              <div class="col-xs-3">
                <a href="https://www.instagram.com/pikinglishclassroom/">
                  <i class="fa fa-instagram"></i>
                </a>
              </div>

              <div class="col-xs-3">
                <a
                  href="https://www.youtube.com/channel/UC7IaqQi_m8PUEKgQRh5RZww?view_as=subscriber"
                >
                  <i class="fa fa-youtube"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </nav>
    </div>

    <!-- Main content -->
    <div id="app">
      <div class="row" id="contenidos">
        <!-- Presentation -->
        <div id="contenidoTexto" class="col-md-12" style="margin: 0">
          <div class="col-sm-1"></div>
          <div id="textoIntroTitulo" class="container-sm">
            <span style="text-shadow: 1em black"
              >¡ESTÁS A UN PASO DE APRENDER INGLÉS CON LOS MEJORES
              MAESTROS!</span
            >
          </div>
        </div>

        <!-- Registration Form -->
        <div class="row" id="contenidoRegister">
          <div class="col-md-12">
            <b-form @submit="onSubmit" v-if="show">
              <!-- Name field -->
              <b-form-group
                id="input-group"
                label="Nombre:"
                label-for="input-1"
                description="Proporciona tu nombre completo."
              >
                <b-form-input
                  id="input-1"
                  v-model="form.name"
                  required
                  placeholder="Ingresa tu nombre"
                ></b-form-input>
              </b-form-group>

              <!-- surName field -->
              <b-form-group
                id="input-group"
                label="Tu apellido:"
                label-for="input-2"
              >
                <b-form-input
                  id="input-2"
                  v-model="form.surName"
                  required
                  placeholder="Ingresa tu apellido"
                ></b-form-input>
              </b-form-group>

              <!-- email fielddd -->
              <b-form-group
                id="input-group"
                label="Tu correo:"
                label-for="input-3"
              >
                <b-form-input
                  id="input-3"
                  v-model="form.email"
                  required
                  placeholder="Ingresa tu email"
                ></b-form-input>
              </b-form-group>

              <!-- password field -->
              <b-form-group
                id="input-group"
                label="Tu contraseña:"
                label-for="input-4"
              >
                <b-form-input
                  id="input-4"
                  type="password"
                  v-model="form.password"
                  required
                  placeholder="Ingresa tu contraseña"
                ></b-form-input>
              </b-form-group>

              <!-- confirm password field -->
              <b-form-group
                id="input-group"
                label="Repite tu contraseña:"
                label-for="input-5"
              >
                <b-form-input
                  id="input-5"
                  type="password"
                  v-model="form.confpassword"
                  required
                  placeholder="Ingresa tu contraseña nuevamente"
                ></b-form-input>
              </b-form-group>

              <b-button type="submit" variant="primary">Submit</b-button>
            </b-form>
            <b-card class="mt-3" header="Form Data Result">
              <pre class="m-0">{{ form }}</pre>
            </b-card>
          </div>
        </div>
      </div>
    </div>
    <footer>
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-6" id="contenidos-footer">
            <div class="row"><h4 id="agrwi">agreement with</h4></div>
            <div class="row">
              <div class="col-sm-2"></div>
              <div class="col-sm-3">
                <img
                  id="logoPa"
                  src="/custompages/footer/americanLand.jpg"
                  alt="americanLand"
                />
              </div>
              <div class="col-sm-2"></div>
              <div class="col-sm-3" id="logoPa">
                <img
                  id="logoPa"
                  src="/custompages/footer/Umas.png"
                  alt="Umas"
                />
              </div>
            </div>
          </div>
          <div class="vertical-line"></div>
          <div class="col-md-5" id="contenidos-footer">INFORMACION FOOTER</div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import SignIn from "./components/SignIn";
import Sliders from "./components/Sliders";
import infoSliders from "./components/infoSliders";
import Testimonios from "./components/Testimonios";
export default {
  name: "App",
  data() {
    return {
      vue: {
        login: false,
        numSlider: 0,
      },
      form: {
        name: "",
        surName: "",
        email: "",
        password: "",
        confpassword: "",
      },
      show: true,
    };
  },
  components: {
    SignIn,
    Sliders,
    infoSliders,
    Testimonios,
  },
  methods: {
    animacion() {
      if (!this.vue.login) {
        this.setLogin(true);
      } else {
        this.setLogin(false);
      }
    },
    setLogin(k) {
      console.log(k + "ey ");
      this.vue.login = k;
    },
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
  },
};
</script>

<style>
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-weight: 600;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  height: 200%;
}
#header {
  font-weight: 600;
  font-size: 1.5em;
  /**background:  rgb(234,84,72);**/
}

#agrwi {
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 0;
}

.row {
  text-align: center;
}

#logo {
  height: 100px;
  padding-top: 0;
  padding-bottom: 0;
}

.body {
  width: 100%;
  height: 100%;
  margin: auto;
}

#iconoSocial {
  margin-top: auto;
  margin-bottom: auto;
}

#contenidos-header,
#contenidos-footer {
  font-family: sans-serif;
  font-size: 150%;
  margin-top: auto;
  margin-bottom: auto;
}

#contenidos-footer {
  padding-top: auto;
  padding-bottom: auto;
}

#contenidos {
  font-weight: 600;
  width: 100%;
  margin: 0em;
  padding-top: 2em;
  padding-bottom: 2em;
}

#contenidoRegister {
  font-weight: 600;
  width: 100%;
  margin-left: 20em;
  margin-right: 20em;
  padding-top: 2em;
  padding-bottom: 2em;
}
#testimonios {
  margin: auto;
}
.navbar-toggler {
  float: right;
}

#logoPa {
  height: 3em;
}

.vertical-line {
  border-style: solid;
  border-radius: 1em;
  border-color: rgb(234, 84, 72);
}
#itemsNavBar {
  text-align: center;
  padding: 2%;
}

#textoIntro {
  font-weight: 700;
  margin-right: 4%;
  margin-left: 4%;
  padding-right: 0em;
}

#botontoggle {
  margin: auto;
}

#textoIntroTitulo {
  color: rgb(15, 103, 177);
  font-family: "Inder";
  font-size: 3.5em;
}

#logo-area {
  width: 2em 120%;
}

.ripple {
  background-position: center;
  transition: background 0.8s;
}
.ripple:hover {
  background: #47a7f5 radial-gradient(circle, transparent 1%, #47a7f5 1%)
    center/15000%;
}
.ripple:active {
  background-color: rgb(234, 84, 72);
  background-size: 100%;
  transition: background 0s;
}

/* Button style */
.ripple {
  border: none;
  border-radius: 1em;
  padding: 1em;
  font-size: 16px;
  text-transform: uppercase;
  cursor: pointer;
  color: white;
  background-color: rgb(234, 84, 72);
  width: 100%;
}

#itemsNavBarBoton {
  padding-top: 2%;
  padding-bottom: 2%;
}

#fixed-top-colapse {
  width: 100%;
}

#input-group{
  text-align:left
}

@media screen and (max-width: 990px) {
  #fixed-top-colapse {
    margin-bottom: 0.8em;
  }
  #iconoSocial {
    width: 250%;
  }
}

#contenerdorTextoPresentacion,
#textoIntro {
  padding: 0em;
  margin: 0px;
}

#contenidoLogin {
  animation-duration: 1s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    left: -100%;
  }
  to {
    left: 0%;
  }
}

.col-xs-3 {
  width: 25%;
}
</style>
