<script>

export default{
  name: 'MainContactUs'
}

</script>

<template>

  <section>

    <div class="container">
      <h2>Want to work with us? Send us <span class="accent_text">a message!</span></h2>
      <p class="content_text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commo.</p>
      <button class="btn btn_green">
        <span>Contact</span>
      </button>
    </div>

  </section>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

section{
  background-image: url(../assets/img/contact-back-img-1.png);
  background-size: cover;
  padding-top: 150px;
  padding-bottom: 100px;
}

.container{
  padding-inline: 0;
  text-align: center;

  h2,p{
    margin-bottom: 40px;
  }

  button{
    padding-inline: 60px;
  }
}

</style>