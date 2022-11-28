<script>

import BlogArticle from './BlogArticle.vue';

export default{
  name: 'MainBlog',
  components:{
    BlogArticle
  }
}

</script>

<template>

  <section id="blog">

    <div class="container">

      <BlogArticle
        title="This way, loves: a detailed guide through new design" 
        author="By Emily Fields" 
        dateDay="12" 
        dateMonth="AUG '21" 
        imgBack="h-2-blog-img-1.jpg"
      />

      <BlogArticle
        title="I try to give people a different way of looking art" 
        author="By Emily Fields" 
        dateDay="07" 
        dateMonth="JAN '20" 
        imgBack="h-2-blog-img-2.jpg"
      />

      <BlogArticle
        title="Introduce Richard Laperrière of those amazing features" 
        author="By Emily Fields" 
        dateDay="22" 
        dateMonth="MAY '19" 
        imgBack="h-2-blog-img-3.jpg"
      />

    </div>


  </section>

</template>

<style lang="scss" scoped>

#blog{
  padding-block: 125px;
}

.container{
  display: flex;
  justify-content: space-between;
}

</style>