<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default{
  name: 'App',
  data(){
    return{
      headerMenuItems: ['home', 'pages', 'portfolio', 'blog', 'shop', 'elements'],
      activePage: 'home'
    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter
  }
}

</script>

<template>

  <AppHeader :menuItems="headerMenuItems" :active="activePage"/>
  <AppMain/>
  <AppFooter/>

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>
