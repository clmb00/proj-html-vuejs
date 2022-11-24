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

    <div class="jumbo_container">
      <MainJumbotron/>
    </div>

    <section>
      <MainSectionSquares/>
    </section>

    <section>
      <MainSectionProcess/>
    </section>

    <section>
      <MainContactUs/>
    </section>

    <section>
      <MainBlog/>
    </section>

  </main>

</template>

<style lang="scss" scoped>

</style>