<template lang="pug">
.all
        .tt Tin tuc 
        list 
            .l.be Đăng ký convert
            .l.tr Bảng lương convert
            .l.be Kiếm tiền với tàng thư viện
            .l.tr Các đơn vị tiền tệ
            .l.be Các bước trở thành converter
            
</template>
<script>
export default {
    name: 'tintuc'
}
</script>
<style lang="stylus" scoped>
    .all
        display flex
        flex-direction column
        width 25%
        margin 10px
    .tt
        background-color white 
        padding auto
        text-align center
        font-size 20px 
        font-weight bold
    
    .l
        width 100%
        padding 5px 10px
        font-size 18px
    .be 
        background-color: pink

    .tr
        background-color white
</style>
