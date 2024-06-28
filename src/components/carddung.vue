<template lang="pug">

div.slidecontainer
    div.slidecontainer__anh
    //-   img(:src='`${avatar}`' class='slidecontainer__image')
    div.slidecontainer__ten {{ tentruyen }}
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
    }
   
  },
  computed: {
    
  },
};
</script>

<style lang="stylus" scoped>
  shdw = 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.2)
  
  .slidecontainer
    box-shadow shdw;
    background-color #ffffff
    border-radius 10px
    padding 10px
    width 30%
    height 50px
    margin 5px
    &__anh
        
    &__image
        border-radius 8%
        object-fit contain

    &__ten
      font-size 20px
      font-weight 20px
    
</style>