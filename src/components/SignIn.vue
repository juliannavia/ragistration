<template>
  <div class="login">
    <div id="login-form-box" class="form-box"></div>

    <form
      id="login-form"
      class="form"
      action="<?php echo api_get_path(WEB_PATH); ?>index.php"
      method="post"
    >
      <h3 id="textLogin">ACCESO</h3>
      <div class="form-group">
        <label id="textLogin" for="login" action>USUARIO</label>
        <input name="login" type="text" class="form-control form-control-lg" />
      </div>
      <div class="form-group">
        <label id="textLogin" for="password">CONTRASEÑA</label>
        <input name="password" type="password" class="form-control form-control-lg" />
      </div>
      <button
        type="submit"
        class="btn btn-lg btn-block form-submit"
        onclick="document.forms['login-form'].submit();"
      >ENTRAR</button>
      <span
        class="forgot-password text-right mt-2 mb-4"
        id="textLogin"
        href="<?php echo api_get_path(WEB_CODE_PATH); ?>auth/lostPassword.php?language=<?php echo api_get_interface_language(); ?>"
      >¿OLVIDASTE TU CONTRASEÑA?</span>
    </form>
  </div>
</template>


<script>
import axios from "axios";

export default {
  name: "Login",
  data: {},
  data() {
    return {
      Mensaje1: "LOGIN",
    };
  },
  methods: {
    load: function (url) {
      axios
        .get(url, {
          headers: { "X-Requested-With": "XMLHttpRequest" },
        })
        .then(
          (response) => {
            console.log(response.statusText);
            console.log(response.WEB_PATH);
            console.log(api_get_path("WEB_PATH"));
            console.log("hola");
          },
          function () {
            alert("ERROR");
          }
        );
    },
    mounted() {
      this.load("https://classroom.pikinglish.com/index.php");
    },
  },
};
</script>

<style scoped>
.login {
  margin: auto;
}

#textLogin {
  color: white;
}

.btn-lg {
  font-weight: 700;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  background: rgb(234, 84, 72);
  color: white;
}
</style>
