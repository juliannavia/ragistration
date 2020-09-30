<template>
  <div>
    <div class="row" id="cuadro">
      <div class="col-md-12" id="textoPresentacion" v-if="numero == 0">
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <span id="numero">2</span>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text" style="font-size: 0.2em;">TIPOS DE VERBOS</p>
          </div>
        </div>
        <div class="row" >
        <div class="col-sm-2"></div>
          <div class="col-sm-8" id="linea"></div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text2">Regulares e Irregulares.</p>
          </div>
        </div>
        <div class="col-sm-2"></div>
      </div>
      <div class="col-md-12" id="textoPresentacion" v-if="numero == 1">
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <span id="numero">4</span>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text" style="font-size: 0.2em;"> FORMAS DE ESCRIBIR UN VERBO</p>
          </div>
        </div>
        <div class="row" >
        <div class="col-sm-2"></div>
          <div class="col-sm-8" id="linea"></div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text2">Presente, Pasado, Participio Y Progresivo</p>
          </div>
        </div>
        <div class="col-sm-2"></div>
      </div>
      <div class="col-md-12" id="textoPresentacion" v-if="numero == 2">
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <span id="numero">5</span>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text" style="font-size: 0.21em;">MODIFICADORES DEL TIEMPO</p>
          </div>
        </div>
        <div class="row" >
        <div class="col-sm-2"></div>
          <div class="col-sm-8" id="linea"></div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text2">Do, Does, Did, Will y Would</p>
          </div>
        </div>
        <div class="col-sm-2"></div>
      </div>
      <div class="col-md-12" id="textoPresentacion" v-if="numero == 3">
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <span id="numero">12</span>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text" style="font-size: 0.21em;">VERBOS CON SÚPER PODER</p>
          </div>
        </div>
        <div class="row" >
        <div class="col-sm-2"></div>
          <div class="col-sm-8" id="linea"></div>
        </div>
        <div class="row">
          <div class="col-sm-2"></div>
          <div class="col-sm-8">
            <p id="text2">Have-Has-Had /Is-Am-Are-Was-Were/Can-Could-Should-Must</p>
          </div>
        </div>
        <div class="col-sm-2"></div>
      </div>      
    </div>
  </div>
</template>


<style scoped>
#textoPresentacion {
  font-family: "Old English Text MT";
  font-size: 8em;
  padding: 0;
}

#linea{
  border-style: solid;
  border-width: 2px;
  border-radius: 1em;
  border-color: rgb(234, 84, 72);
}

/deep/.row {
  margin: 0;
}

#text {  
  font-family: 'Inder';
  font-size: 0.3em;
}
#text2 {  
  margin-top: 1em;
  font-family: 'Inder';
  font-style: italic;
  font-size: 0.2em;
}

#numero{
  color: rgb(234, 84, 72);
}

@media screen and (min-width: 990px) {
  #textLG {
    font-size: 170%;
  }
}
</style>

<script>
export default {
  data() {
    return {};
  },
  props: ["numero"],
};
</script>