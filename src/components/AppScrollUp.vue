<script>

export default{
  name: 'AppScrollUp',
  data(){
    return{
      hideScrollUp: true,
    }
  },
  methods:{
    scrollTop(){
      window.scrollTo(0,0);
    }
  },
  mounted(){
    window.addEventListener('scroll', ()=>{
      (window.scrollY > 300) ? this.hideScrollUp = false : this.hideScrollUp = true;
    });
  }
}

</script>

<template>

  <div class="scroll_to_top" :class="{'hide' : hideScrollUp}" @click="scrollTop()"></div>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.scroll_to_top{
  width: 50px;
  height: 50px;
  position: fixed;
  z-index: 999;
  bottom: 50px;
  right: 25px;
  box-shadow: 0 0 4px 1px $black-trasparent;
  background-color: $back-green-dark;
  text-align: center;
  padding-top: 14px;
  cursor: pointer;
  user-select: none;
  transition: all .3s ease;
  &:hover{
    background-color: $back-pink-normal;
  }
  &:active{
    transform: scale(.95);
  }
  &::after{
    content: url(../assets/svg/svg-2.svg);
  }
  &.hide{
    opacity: 0;
  }
}

</style>