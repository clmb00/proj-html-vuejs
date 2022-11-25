<script>

export default{
  name: 'MainSectionSquares'
}

</script>

<template>

  <section>

    <div class="squares_container">
      <div class="square">
        <img src="../assets/img/h-2-port-img-1.jpg" alt="">
        <div class="sq_descr">
          <h3>Designs of Logos</h3>
          <p>Design</p>
        </div>
      </div>
      <div class="square">
        <img src="../assets/img/h-2-port-img-2.jpg" alt="">
        <div class="sq_descr">
          <h3>Graphics of cartoons</h3>
          <p>Graphics</p>
        </div>
      </div>
      <div class="square">
        <img src="../assets/img/h-2-port-img-3.jpg" alt="">
        <div class="sq_descr">
          <h3>Illustrations of books</h3>
          <p>Illustration</p>
        </div>
      </div>
      <div class="square">
        <img src="../assets/img/h-2-port-img-4.jpg" alt="">
        <div class="sq_descr">
          <h3>Illustrations of novels</h3>
          <p>Illustration</p>
        </div>
      </div>
      <div class="square">
        <img src="../assets/img/h-2-port-img-5.jpg" alt="">
        <div class="sq_descr">
          <h3>Designs of apps</h3>
          <p>Design</p>
        </div>
      </div>
      <div class="square">
        <img src="../assets/img/h-2-port-img-6.jpg" alt="">
        <div class="sq_descr">
          <h3>Graphics of characters</h3>
          <p>Graphic</p>
        </div>
      </div>
    </div>

  </section>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.squares_container{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  .square{
    width: calc(100% / 3);
    aspect-ratio: 1/1;
    position: relative;
    cursor: pointer;
    overflow: hidden;
    img{
      min-height: 100%;
      transition: all .5s ease;
    }
  }
  .sq_descr{
    position: absolute;
    top: calc(50% - 60px);
    left: 0;
    height: 100px;
    padding-top: 18px;
    padding-inline: 22px;
    background-color: $white;
    box-shadow: 3px 0 3px .5px $black-trasparent;
    transition: all .8s ease;
    transform: translateX(-102%);
    h3{
      font-size: 1.3rem;
      font-weight: 400;
      margin-bottom: 5px;
    }
    p{
      font-style: italic;
      font-family: $accent-font;
    }
  }

  .square:hover{
    & img{
      transform: scale(1.1);
      filter: brightness(.9);
    }
    & .sq_descr{
      transform: translateX(0) scaleX(1);
    }
  }
}

</style>