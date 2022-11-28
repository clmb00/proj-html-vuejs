<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppScrollUp from './components/AppScrollUp.vue';

export default{
  name: 'App',
  data(){
    return{
      headerMenuItems: ['home', 'pages', 'portfolio', 'blog', 'shop', 'elements'],
      contacts: {
        email: 'maree.qode@gmail.com',
        phone: '+44645 321 789',
        address: "Avenue d'Auderghem 10",
        city: '1040 Brussels, Belgium'
      },
      startPage: 'home'
    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter,
    AppScrollUp
  }
}

</script>

<template>

  <AppHeader :menuItems="headerMenuItems" :active="startPage"/>
  <AppMain/>
  <AppFooter :contacts="contacts"/>
  <AppScrollUp/>

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>
