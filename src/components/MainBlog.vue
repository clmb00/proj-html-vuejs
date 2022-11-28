<script>

import BlogArticle from './BlogArticle.vue';

export default{
  name: 'MainBlog',
  data(){
    return{
      articles: [
        {
          id: 1,
          title: 'This way, loves: a detailed guide through new design',
          author: 'By Emily Fields',
          dateDay: '12',
          dateMonth: "AUG '21",
          imgBack: 'h-2-blog-img-1.jpg'
        },{
          id: 2,
          title: 'I try to give people a different way of looking art',
          author: 'By Emily Fields',
          dateDay: '07',
          dateMonth: "JAN '20",
          imgBack: 'h-2-blog-img-2.jpg'
        },{
          id: 3,
          title: 'Introduce Richard Laperrière of those amazing features',
          author: 'By Emily Fields',
          dateDay: '22',
          dateMonth: "MAY '19",
          imgBack: 'h-2-blog-img-3.jpg'
        }
      ]
    }
  },
  components:{
    BlogArticle
  }
}

</script>

<template>

  <section id="blog">

    <div class="container">

      <BlogArticle v-for="article in articles" :key="article.id"
        :title="article.title" 
        :author="article.author" 
        :dateDay="article.dateDay" 
        :dateMonth="article.dateMonth" 
        :imgBack="article.imgBack"
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
  flex-wrap: wrap;
  row-gap: 40px;
  justify-content: space-between;
}

@media screen and (max-width: 768px) {
  .container{
    flex-direction: column;
    align-items: center;
  }
}

</style>