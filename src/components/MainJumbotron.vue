<script>

import CompSlide from './CompSlide.vue';

export default{
  name: 'MainJumbotron',
  components:{
    CompSlide,
  },
  data(){
    return{
      indexSlider: 1
    }
  },
  methods:{
    slide(direction){
      if (direction == 'left'){
        if (--this.indexSlider == 0) this.indexSlider = 3
      } else {
        if (++this.indexSlider == 4) this.indexSlider = 1
      };
    }
  }
}
</script>

<template>

  <div class="jumbotron">

    <div class="arrow arrow_left" @click="slide('left')">
      <i class="fa-solid fa-chevron-left"></i>
    </div>

    <CompSlide
      title="Devotion that never " 
      accentTitle="ends"
      descr="Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi." 
      button="Read more" 
      :indexSlider="indexSlider" 
      :slideNumber="1"
    />

    <CompSlide
      title="Inspiration that never " 
      accentTitle="stop"
      descr="Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi." 
      button="Find more" 
      :indexSlider="indexSlider" 
      :slideNumber="2"
    />

    <CompSlide
      title="Designs made with " 
      accentTitle="love"
      descr="Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi." 
      button="Read more" 
      :indexSlider="indexSlider" 
      :slideNumber="3"
    />

    <div class="arrow arrow_right" @click="slide('right')">
      <i class="fa-solid fa-chevron-right"></i>
    </div>

    <div class="pagSlider">
      <div class="pag" :class="{'active' : indexSlider == 1}" @click="indexSlider = 1"></div>
      <div class="pag" :class="{'active' : indexSlider == 2}" @click="indexSlider = 2"></div>
      <div class="pag" :class="{'active' : indexSlider == 3}" @click="indexSlider = 3"></div>
    </div>

  </div>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.jumbotron{
  height: $jumbo-height;
  position: relative;
  margin-bottom: 90px;
}

.arrow{
  width: 30px;
  height: 30px;
  border-radius: 50%;
  text-align: center;
  line-height: 30px;
  background-color: $back-pink-normal;
  color: white;
  top: calc(50% - 15px);
  position: absolute;
  z-index: 998;
  cursor: pointer;
  &.arrow_left{
    left: 2rem;
  }
  &.arrow_right{
    right: 2rem;
  }
}

.pagSlider{
  width: 100%;
  padding-top: 50px;
  padding-bottom: 40px;
  margin: 0px auto;
  display: flex;
  justify-content: center;
  column-gap: 25px;
  cursor: pointer;
  user-select: none;
  .pag{
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: $back-pink-normal;
    transition: all .4s ease;
    &.active{
      width: 15px;
      height: 15px;
    }
  }
}

</style>