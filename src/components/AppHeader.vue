<script>

export default{
  name: 'AppHeader'
}

</script>

<template>

  <header>

    <div id="header_logo">
      <img src="../assets/img/logo-sidearea-1.png" alt="Marée Logo">
    </div>

    <nav id="header_nav">

      <ul class="menu_nav">
        <li><a href="#">Home</a></li>
        <li><a href="#">Pages</a></li>
        <li><a href="#">Portfolio</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Elements</a></li>
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
  --spacing-btw-elements: 50px;
  display: flex;
  .menu_nav{
    display: flex;
    column-gap: var(--spacing-btw-elements);
    a{
      text-transform: uppercase;
      font-size: .8rem;
      font-weight: 700;
      letter-spacing: .2rem;
    }
  }
  .menu_icon{
    width: 25px;
    aspect-ratio: 1/1;
    margin-left: var(--spacing-btw-elements);
  }
}

</style>