<script>

export default{
  name: 'AppHeader',
  props:{
    menuItems: Array,
    active: String
  }
}

</script>

<template>

  <header>

    <div id="header_logo">
      <a href="#">
        <img src="../assets/img/logo-sidearea-1.png" alt="Marée Logo">
      </a>
    </div>

    <nav id="header_nav">

      <ul class="menu_nav">
        <li v-for="(elem, index) in menuItems" :key="index" :class="{'active_class' : elem == active}"><a href="#" @click="active = elem">{{elem}}</a></li>
      </ul>

      <button class="menu_icon">
        <img src="../assets/svg/svg-1.svg" alt="#">
      </button>

    </nav>

  </header>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

header{
  width: 100%;
  height: $header-height;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-inline: 2rem;
}

#header_logo{
  width: 110px;
}

#header_nav{
  --spacing-btw-elements: 44px;
  display: flex;
  .menu_nav{
    display: flex;
    column-gap: var(--spacing-btw-elements);
    li{
      padding-inline: 2px;
      position: relative;
      &::before{
        content: '';
        width: 100%;
        height: 25%;
        background-color: $back-pink-dark;
        position: absolute;
        bottom: 25%;
        left: 0;
        z-index: -1;
        transform: translateX(-50%) scaleX(0);
        transition: transform .8s ease;
      }
      &.active_class::before{
        transform: translateX(0%) scaleX(1);
      }
      a{
        text-transform: uppercase;
        font-size: .8rem;
        font-weight: 700;
        letter-spacing: .2rem;
      }
    }
  }
  .menu_icon{
    width: 25px;
    aspect-ratio: 1/1;
    margin-left: var(--spacing-btw-elements);
  }
}

@media screen and (max-width: 992px) {
  #header_nav{
    --spacing-btw-elements: 20px;
  }
}

@media screen and (max-width: 768px) {
  #header_nav{
    .menu_nav{
      display: none;
    }
  }
}

</style>