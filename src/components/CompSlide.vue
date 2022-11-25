<script>

export default{
  name: 'CompSlide',
  props:{
    title: String,
    accentTitle: String,
    descr: String,
    button: String,
    indexSlider: Number,
    slideNumber: Number,
    next: Number,
    prev: Number,
    direction: String
  }
}
</script>

<template>

  <div class="slide" :class="{'active' : indexSlider == slideNumber, 'next' : next == slideNumber, 'prev' : prev == slideNumber}">

    <div class="container">
      <div class="text_content">
        <h1>{{title}}<span class="accent_text">{{accentTitle}}</span></h1>
        <p class="content_text">{{descr}}</p>
        <button class="btn btn_pink">{{button}}</button>
      </div>
    </div>
  
    <div class="images_content">
      <img id="img_01" src="../assets/img/h-2-slider-img-13.png" alt="">
      <img id="img_02" src="../assets/img/h-2-slider-img-17.png" alt="">
      <img id="img_03" src="../assets/img/h-2-slider-img-12.png" alt="">
      <img id="img_04" src="../assets/img/h-2-slider-img-14.png" alt="">
      <img id="img_05" src="../assets/svg/svg-0.svg" alt="">
      <img id="img_06" src="../assets/svg/svg-0.svg" alt="">
      <img class="img_main" :class="{'img_A1' : slideNumber == 1}" src="../assets/img/h-2-slider-img-15.png" alt="">
      <img class="img_main" :class="{'img_A2' : slideNumber == 1}" src="../assets/img/h-2-slider-img-16.png" alt="">
      <img class="img_main" :class="{'img_B1' : slideNumber == 2}" src="../assets/img/h-2-slider-img-11.png" alt="">
      <img class="img_main" :class="{'img_C1' : slideNumber == 3}" src="../assets/img/short-slider-rev-1-img-3.png" alt="">
    </div>

  </div>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.slide{
  width: 100%;
  height: 100%;
  // flex-shrink: 0;
  align-items: center;
  position: relative;
  // display: none;
  transition: transform 1s ease, visibility 1s ease;
  background-color: white;
  position: absolute;
  &.active{
    transform: translateX(0%);
    z-index: 500;
  }
  &.next{
    transform: translateX(100%);
    visibility: hidden;
  }
  &.prev{
    transform: translateX(-100%);
    visibility: hidden;
  }
}

.text_content{
  width: 50%;
  padding-right: 1rem;
  height: 450px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}

h1{
  font-size: 5rem;
  font-weight: 300;
  line-height: 5rem;
  // Per allinearlo al p e button, visto che il font size grande sposta l'inizio delle prime lettere del h1
  margin-left: -3px;
}

h1, p{
  margin-bottom: 40px;
}

.images_content{
  position: absolute;
  left: 50%;
  top: 0;
  width: 50%;
  max-height: $jumbo-height;
  aspect-ratio: 1.7/1;
  img{
    position: absolute;
  }
  #img_01{
    height: 15%;
    bottom: 0;
    left: 2%;
  }
  #img_02{
    height: 25%;
    bottom: 0;
    right: 15%;
  }
  #img_03{
    height: 8%;
    bottom: 40%;
    left: -2%;
  }
  #img_04{
    height: 12%;
    top: 8%;
    left: 65%;
  }
  #img_05{
    height: 10%;
    top: 10%;
    left: 8%;
    transform: scale(-1, 1)
  }
  #img_06{
    height: 10%;
    top: 30%;
    right: 25%;
  }
  .img_main{
    display: none;
  }
  .img_A1{
    display: block;
    height: 80%;
    bottom: 0;
    right: 55%;
  }
  .img_A2{
    display: block;
    height: 80%;
    bottom: 0;
    left: 40%;
  }
  .img_B1{
    display: block;
    height: 80%;
    bottom: 0;
    left: 10%;
  }
  .img_C1{
    display: block;
    height: 80%;
    bottom: 0;
    left: 13%;
  }
}

</style>