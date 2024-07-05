<template lang="pug">
.bar
        a(href="#")
            .tool
                i.fa.fa-bar-chart
                .title Xếp hạng 
        a(href="#")
            .tool
                i.fas.fa-filter
                .title Bộ lọc
        a(href="#")
            .tool
                i.fas.fa-crown
                .title Top users
        a(href="#")
            .tool
                i.fa.fa-book
                .title Review 
.pc     
    ul.nav.nav-tabs.custom-navbar
        li.nav-item
            a.nav-link.active(href='#') Trang chủ
        li.nav-item
            a.nav-link(href='#') Bộ lọc
        li.nav-item
            a.nav-link(href='#') Reviews
        li.nav-item
            a.nav-link(href='#') Cửa hàng
        li.nav-item
            a.nav-link(href='#') Bảng xếp hạng

</template>

<script>
export default {
    name: 'toolbar',
}
</script>

<style lang="stylus" scoped>
    a 
            color inherit /* This will inherit the color from its parent */
            text-decoration none /* Optional: Remove underline */
    a:hover
            color: #2798a1
    @media (min-width: 1024px) 
        .bar
            display: none
        .pc 
            display: flex
            justify-content center
            padding-top 20px
            font-size: 20px

      
    @media (max-width: 412px)
        .pc 
            display: none
        .bar
            display flex
            padding-top 20px 
            justify-content center
        
        .tool
            display flex
            flex 1 1 20%;
            flex-direction column
            justify-content center
            align-items center
            margin 0 15px
        i
            font-size 30px
            color #2798a1
        .title
            margin 10px 0 0
            font-weight bold
</style>