<script>

export default{
  name: 'BlogArticle',
  props: {
    title: String,
    author: String,
    dateDay: Number,
    dateMonth: String,
    imgBack: String
  },
  computed: {
    byAuthor(){
      return 'By ' + this.author
    }
  }
}
</script>

<template>

  <article>
    <img :src="'src/assets/img/' + imgBack" :alt="imgBack">
    <h3>{{title}}</h3>
    <p>{{byAuthor}}</p>
    <div class="tag">
      <p class="accent_text">{{dateDay}}</p>
      <p>{{dateMonth}}</p>
    </div>
  </article>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

article{
  width: 32%;
  position: relative;
  cursor: pointer;
  img{
    max-height: 260px;
  }
  h3{
    font-weight: 400;
    font-size: 1.4rem;
    margin-top: 24px;
  }
  &>p{
    font-style: italic;
    font-family: "Playfair Display", sans-serif;
    font-size: .8rem;
    margin-top: 15px;
  }
  .tag{
    position: absolute;
    top: -20px;
    left: 20px;
    text-align: center;
    p:first-child{
      font-size: 2.1rem;
      background-color: $back-green-dark;
      padding: 0px 12px 10px;
      line-height: 2.2rem;
    }
    p:last-child{
      text-transform: uppercase;
      font-size: .7rem;
      font-weight: 700;
      background-color: $back-pink-normal;
      position: relative;
      padding-block: 5px;
      &::before{
        content: '';
        position: absolute;
        top: 100%;
        left: 0;
        width: 50%;
        height: 15px;
        background: linear-gradient(to top left, rgba(0,0,0,0) 0%, rgba(0,0,0,0)48%, $black-trasparent 48%, $back-pink-normal 52%, $back-pink-normal 100%);
      }
      &::after{
        content: '';
        position: absolute;
        top: 100%;
        right: 0;
        width: 50%;
        height: 15px;
        background: linear-gradient(to top right, rgba(0,0,0,0) 0%, rgba(0,0,0,0)48%, $black-trasparent 48%, $back-pink-normal 52%, $back-pink-normal 100%);
      }
    }
  }
}

@media screen and (max-width: 768px) {

  article{
    width: 90%;
    img{
      max-height: none;
    }
    h3{
      font-weight: 700;
    }
  }
}

</style>