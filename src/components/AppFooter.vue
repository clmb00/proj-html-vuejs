<script>

export default{
  name: 'AppFooter',
  props:{
    contacts: {
      email: String,
      phone: String,
      address: String,
      city: String
    }
  }
}

</script>

<template>

  <footer>

    <div class="container">

      <div class="footer_logo">
        <div class="logo">
          <a href="#">
            <img src="../assets/img/logo-sidearea-1.png" alt="">
          </a>
        </div>
        <p>Let's Get Creative</p>
      </div>

      <div class="grid">
        <p>{{contacts.email}}</p>
        <p>{{contacts.address}}</p>
        <p>Stay in touch with us</p>
        <p>{{contacts.phone}}</p>
        <p>{{contacts.city}}</p>
        <div class="socials">
          <a href="#"><i class="fa-brands fa-twitter twitter-color"></i></a>
          <a href="#"><i class="fa-brands fa-pinterest-p pint-color"></i></a>
          <a href="#"><i class="fa-brands fa-facebook-f facebook-color"></i></a>
          <a href="#"><i class="fa-brands fa-linkedin-in linkedin-color"></i></a>
        </div>
      </div>

      <!-- <div class="footer_cell">
      </div>

      <div class="footer_cell">
      </div>

      <div class="footer_cell">
      </div> -->


    </div>


  </footer>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

footer{
  background-color: $back-green-dark;
  padding-block: 65px;
  font-size: .9rem;
}

.container{
  --gap-columns: 8vw;
  display: flex;
}

.footer_logo{
  margin-right: var(--gap-columns);
  .logo{
    margin-bottom: 5px;
  }
}

.grid{
  display: grid;
  grid-template-columns: auto auto auto;
  column-gap: var(--gap-columns);
  row-gap: 10px;
  .socials{
    width: 100%;
    display: flex;
    justify-content: space-between;
    i{
      font-size: 1.1rem;
      &.facebook-color:hover{
        color: #1877f2;
      }
      &.twitter-color:hover{
        color: #1d9bf0;
      }
      &.pint-color:hover{
        color: #e60023;
      }
      &.linkedin-color:hover{
        color: #0a66c2;
      }
    }
  }
}

@media screen and (max-width: 992px) {
  .grid{
    grid-template-columns: auto auto;
    p:nth-child(3){
      order: 1;
    }
    div{
      order: 2;
    }
  }
}

@media screen and (max-width: 768px) {
  .container{
    --gap-columns: 4vw;
  }
}

@media screen and (max-width: 576px) {
  .container{
    flex-direction: column;
    row-gap: 40px;
  }
  .grid{
    grid-template-columns: auto;
    width: 60%;
    row-gap: 20px;
  }
}

</style>