<script>

export default{
  name: 'MainJumbotron'
}
</script>

<template>

  <div class="jumbotron">

    <div class="container">

      <div class="text_content">
        <h1>Devotion that never <span class="accent_text">ends</span></h1>
        <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.</p>
        <button class="btn btn-pink">Read more</button>
      </div>

    </div>

    <div class="images_content">
      <img id="img_13" src="../assets/img/h-2-slider-img-13.png" alt="">
      <img id="img_15" src="../assets/img/h-2-slider-img-15.png" alt="">
      <img id="img_16" src="../assets/img/h-2-slider-img-16.png" alt="">
      <img id="img_17" src="../assets/img/h-2-slider-img-17.png" alt="">
      <img id="img_12" src="../assets/img/h-2-slider-img-12.png" alt="">
      <img id="img_14" src="../assets/img/h-2-slider-img-14.png" alt="">
      <img id="img_01" src="../assets/svg/svg-0.svg" alt="">
      <img id="img_02" src="../assets/svg/svg-0.svg" alt="">
    </div>


  </div>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.jumbotron{
  height: $jumbo-height;
  display: flex;
  align-items: center;
  position: relative;
  // temporary debug
  margin-bottom: 100px;
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

p{
  color: $text-grey-dark;
}

h1, p{
  margin-bottom: 40px;
}

.images_content{
  position: absolute;
  left: 50%;
  top: 0;
  width: 50%;
  aspect-ratio: 1.7/1;
  img{
    position: absolute;
  }
  #img_13{
    height: 15%;
    bottom: 0;
    left: 2%;
  }
  #img_15{
    height: 80%;
    bottom: 0;
    right: 55%;
  }
  #img_16{
    height: 80%;
    bottom: 0;
    left: 40%;
  }
  #img_17{
    height: 25%;
    bottom: 0;
    right: 15%;
  }
  #img_12{
    height: 8%;
    bottom: 40%;
    left: -2%;
  }
  #img_14{
    height: 12%;
    top: 8%;
    left: 65%;
  }
  #img_01{
    height: 10%;
    top: 10%;
    left: 8%;
    transform: scale(-1, 1)
  }
  #img_02{
    height: 10%;
    top: 30%;
    right: 25%;
  }
}

</style>