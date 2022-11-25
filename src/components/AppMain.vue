<script>

import MainJumbotron from './MainJumbotron.vue';
import MainSectionSquares from './MainSectionSquares.vue';
import MainSectionProcess from './MainSectionProcess.vue';
import MainContactUs from './MainContactUs.vue';
import MainBlog from './MainBlog.vue';

export default{
  name: 'AppMain',
  components:{
    MainJumbotron,
    MainSectionSquares,
    MainSectionProcess,
    MainContactUs,
    MainBlog
  }
}

</script>

<template>
  
  <main>

    <MainJumbotron/>

    <MainSectionSquares/>

    <MainSectionProcess/>

    <MainContactUs/>

    <MainBlog/>

  </main>

</template>

<style lang="scss" scoped>

</style>