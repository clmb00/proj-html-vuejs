<script>

export default{
  name: 'MainSectionProcess'
}

</script>

<template>

  <div class="container">
    <h2>Working <span class="accent_text">process</span></h2>

    <div class="wavy_line">
      <div class="card">
        <div class="logo_card">
          <i class="fa-solid fa-lightbulb green_icon"></i>
        </div>
        <h5>First Theres an idea</h5>
        <p>Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.</p>
      </div>
      <div class="card">
        <div class="logo_card">
          <i class="fa-regular fa-comment ylw_icon"></i>
        </div>
        <h5>Then we talk about</h5>
        <p>Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.</p>
      </div>
      <div class="card">
        <div class="logo_card">
          <i class="fa-solid fa-cloud purp_icon"></i>
        </div>
        <h5>And we think about</h5>
        <p>Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.</p>
      </div>
      <div class="card">
        <div class="logo_card">
          <i class="fa-solid fa-pen-ruler org_icon"></i>
        </div>
        <h5>So we draw along</h5>
        <p>Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.</p>
      </div>
    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.container{
  padding-block: 120px;
  text-align: center;
}

h2{
  font-size: 3.5rem;
  font-weight: 400;
}

.wavy_line{
  background-image: url('../assets/svg/svg-3.svg');
  background-position: top;
  background-repeat: no-repeat;
  background-size: 80%;
  margin-top: 60px;
  // width: 100%;
  display: flex;
  justify-content: space-between;

  .card{
    text-align: center;
    padding-inline: 5px;
    cursor: pointer;
    &:hover .logo_card{
      transform: scale(1.1);
      filter: brightness(.95);
    }
  }

  .logo_card{
    width: 140px;
    height: 140px;
    border-radius: 50%;
    text-align: center;
    line-height: 140px;
    background-color: $back-pink-light;
    font-size: 2.8rem;
    margin: 0 auto;
    transition: transform .5s ease;
    user-select: none;
    .green_icon{
      color: $text-green;
    }
    .ylw_icon{
      color: $text-yellow;
    }
    .org_icon{
      color: $text-orange;
    }
    .purp_icon{
      color: $text-purple;
    }
  }

  h5{
    font-weight: 400;
    font-size: 1.2rem;
    padding: 25px 0px 15px;
  }

  p{
    font-size: .9rem;
    line-height: 1.5rem;
    color: $text-grey-dark;
  }
}

</style>