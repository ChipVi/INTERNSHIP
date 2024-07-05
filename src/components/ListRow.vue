<template lang="pug">
  div(v-for="(each, index) in info" :key="index")
    a(href="#")
      .outerbox
        .outerbox__anh
          img(:src='each.url' class='outerbox__avatar-image')
        .outerbox__content
          .outerbox__ten {{ each.ten }}
          .outerbox__theloai {{ each.rate }}
          star(:rating='each.rate')
</template>

<script>
import star from './star.vue';
export default {
  name: 'user-card-component',
  components:{star},
  props: ['info']
};
</script>

<style lang="stylus" scoped>
 shdw = 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.2)
a
    text-decoration none
    color inherit
  @media (min-width: 1024px) 
    .outerbox
      display flex
      box-shadow shdw;
      background-color #ffffff
      border-radius 10px
      padding 10px
      width 30%
      margin 10px 10px
      align-item center
  @media (max-width: 412px)
    .outerbox
      display flex
      box-shadow shdw;
      background-color #ffffff
      border-radius 10px
      padding 10px
      width 90%
      margin 10px 10px
      align-item center
      &__content
        padding 10px  
        display flex
        flex-direction column
        justify-content center
      &__avatar
        &-image
          border-radius 8%
          width 6rem
      &__theloai
        font-size 15px
        padding 4px
        color #CCC
      &__ten
        font-size 20px
        font-weight 500
    
</style>