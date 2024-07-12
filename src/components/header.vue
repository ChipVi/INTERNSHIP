<template lang="pug">
.header
  h3.d-sm-none TÀNG THƯ VIÊN 
  .imgwr.d-none.d-sm-block
    img(src="../assets/logo-web.png")
  .menu
    .d-none.d-sm-block
      input(type="text" placeholder="Tìm tên truyện hoặc tác giả")
      a(href="#").m-1
          i(class="fas fa-search")
  ul
    li
        a(href="#").d-sm-none
          i(class="fas fa-search")
    li
        a(href="#")
          i(class="fas fa-user-alt")
    li
        a(href="#")
          i(class="fas fa-users")

</template>
<script>
export default {
    name: 'header',
    data() {
    },

}
    
</script>
<style scoped lang="stylus">

    .imgwr
        max-height 95px
        max-width 300px
        margin-left 10px;
    img
        object-fit contain
        width 100%
        height 100%
    .menu{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .header{
        display: flex;
        justify-content:space-between;
        align-items: center;
        background-color: pink;
        padding: 0 10px;
        color: white;
    }
    ul{
        list-style-type: none;
        display:flex;
        flex-direction row
        padding: 0;
    }
    a {
            color: inherit; /* This will inherit the color from its parent */
            text-decoration: none; /* Optional: Remove underline */
    }
    a:hover{
        color: pink;
    }
    i{
        font-size: 25px;
    }
    li{
        margin: 0px 10px ;
    }
    

</style>