<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="6000"
      controls
      indicators
      background="#ababab"      
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide img-src="/custompages/img/1.png">        
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="/custompages/img/2.png" >        
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="/custompages/img/3.png" >        
      </b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide img-src="/custompages/img/4.png" >       
      </b-carousel-slide> 

      <!-- Slide with blank fluid image to maintain slide aspect ratio -->      
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    //en la primera @sliding-start="onSlideStart" ---- @sliding-end="onSlideEnd"
    onSlideStart(slide) {
      this.sliding = true;      
      this.$emit('numSlider', this.slide);
    },
    onSlideEnd(slide) {
      this.sliding = false;
      this.$emit('numSlider', this.slide);
    },
  },
};
</script>

<style scoped>
img{
    width: 100%;
}

#carousel-1{
  background-color: white;
}

/deep/.w-100{
  background-color: white;
}

/deep/.carousel-control-prev-icon, /deep/.carousel-control-next-icon{  
  background-color: grey;
  border-radius: 0.5em;
}

</style>