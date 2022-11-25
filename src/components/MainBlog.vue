<script>

export default{
  name: 'MainBlog'
}

</script>

<template>

  <section id="blog">

    <div class="container">

      <article>
        <img src="../assets/img/h-2-blog-img-1.jpg" alt="Banana">
        <h3>This way, loves: a detailed guide through new design</h3>
        <p>By Emily Fields</p>
        <div class="tag">
          <p class="accent_text">07</p>
          <p>MAY '19</p>
        </div>
      </article>
  
      <article>
        <img src="../assets/img/h-2-blog-img-2.jpg" alt="Town">
        <h3>I try to give people a different way of looking art</h3>
        <p>By Emily Fields</p>
        <div class="tag">
          <p class="accent_text">07</p>
          <p>MAY '19</p>
        </div>
      </article>
  
      <article>
        <img src="../assets/img/h-2-blog-img-3.jpg" alt="Girl">
        <h3>Introduce Richard Laperrière of those amazing features</h3>
        <p>By Emily Fields</p>
        <div class="tag">
          <p class="accent_text">07</p>
          <p>MAY '19</p>
        </div>
      </article>

    </div>


  </section>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

#blog{
  padding-block: 125px;
}

.container{
  display: flex;
  justify-content: space-between;
}

article{
  width: 32%;
  position: relative;
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
    box-shadow: 0 0 5px 1px $black-trasparent;
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
      padding-top: 6px;
      padding-bottom: 12px;
    }
  }
}

</style>