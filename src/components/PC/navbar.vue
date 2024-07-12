<template lang="pug">
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
    name: 'navbar',
}
</script>

<style lang="stylus" scoped>
    a 
            color inherit /* This will inherit the color from its parent */
            text-decoration none /* Optional: Remove underline */
    a:hover
            color: #2798a1
    ul
            display: flex
            justify-content center
</style>