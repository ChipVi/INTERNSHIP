<template lang="pug">
a(href="https://www.youtube.com/watch?v=l6U1JB7z-I8")
  div.outerbox
    div.outerbox__anh
      img(:src='`${avatar}`' class='outerbox__avatar-image')
    div.outerbox__content
      div.outerbox__ten {{ tentruyen }}
      div.outerbox__theloai Thể loại: {{ theloai }}
      div.outerbox__theloai Tình trạng: {{ tinhtrang }}
      div.outerbox__theloai Số chương: {{ sochuong }}

    //- div.user-card-component__action
    //-   button(@click="$emit('contactUser')") Contact {{ lastName }}
</template>

<script>
export default {
  name: 'user-card-component',
  props: {
    avatar: {
      type: String,
    },
    tentruyen: {
      type: String,
    },
    theloai: {
      type: String,
    },
    tinhtrang: {
      type: String,
    },
    sochuong: {
      type: Number,
    },
  },
  computed: {
    
  },
};
</script>

<style lang="stylus" scoped>
  shdw = 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.2)
  a
    text-decoration none
  
  .outerbox
    display flex
    box-shadow shdw;
    background-color #ffffff
    border-radius 10px
    padding 10px
    width 90%
    margin 10 10
    
    &__content
      padding 10px  
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
      margin-top 20px
    
</style>