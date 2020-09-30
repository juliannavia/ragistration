<template>
  <div id="carousel">
    <carousel-3d>
      <slide :index="0">
        <figure>
          <img src="/custompages/img/11.jpg" />
          <figcaption>
            CASI 10 AÑOS ENESÑANDO INGLES
          </figcaption>
        </figure>
      </slide>
      <slide :index="1">
        <figure>
          <img src="/custompages/img/12.jpg" />
          <figcaption>
            VOLUNTARIOS DE TODO EL MUNDO
          </figcaption>
        </figure>
      </slide>
      <slide :index="2">
        <figure>
          <img src="/custompages/img/13.jpg" />
          <figcaption>
            ACTIVIDADES E INTEGRACIONES
          </figcaption>
        </figure>
      </slide>
      <slide :index="3">
        <figure>
          <img src="/custompages/img/14.jpg" />
          <figcaption>
            PROGRAMAS DE INTERCAMBIO
          </figcaption>
        </figure>
      </slide>
      <slide :index="4">
        <figure>
          <img src="/custompages/img/15.jpg" />
          <figcaption>
            AMAMOS LOS ANIMALES
          </figcaption>
        </figure>
      </slide>
      <slide :index="5">
        <figure>
          <img src="/custompages/img/16.jpg" />
          <figcaption>
            SIEMPRE RECORDAMOS LAS FECHAS ESPECIALES
          </figcaption>
        </figure>
      </slide>
    </carousel-3d>
  </div>
</template>


<script>
import { Carousel3d, Slide } from "vue-carousel-3d";
export default {
  data() {
    return {
      slide: 0,
    };
  },
  components: {
    Carousel3d,
    Slide,
  },
  methods: {
    cambiar() {
      if (slide + 1 < 5) {
        slide = 0;
      } else {
        slide = slide + 1;
      }
    },
  },
};
</script>

<style scoped>
.carousel-3d-container figure {
  margin: 0;    
}

.carousel-3d-container figcaption {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  bottom: 0;
  position: absolute;
  bottom: 0;
  padding: 15px;
  font-size: 12px;
  min-width: 100%;
  box-sizing: border-box;
}
img{   
}
</style>