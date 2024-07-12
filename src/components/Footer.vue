<template lang="pug">
.footer1.d-sm-none
        .icon
            span Android
            span iOS
            span PC 
        p Copyright (c) 2014 Thunderagon Development Team

.d-none.d-sm-block
    <br>
    .footer2.text-left
        .imgwr 
            img(src="../assets/logo-web.png")
        .texti
            .d Copyright (c) 2014 Thunderagon Development Team
            .d Tàng Thư Viện là sân chơi mở và free cho cộng đồng fan kiếm hiệp, tiên hiệp, ngôn tình. Chúc các bạn có những giây phút thư giãn thoải mái sau giờ làm việc và học tập căng thẳng.
</template>

<script>
export default {
    name: 'footer',
}
</script>

<style lang="stylus" scoped>
    .icon 
        display flex
        justify-content center
        padding 10px 0 0px
    span
        font-size 20px
        color black
        margin-right 15px
    span:hover
        color gray
    .footer1 
        display flex
        flex-direction column
        align-items center
        background-color white 
    .footer2
        display flex
        flex-direction row
        padding 10px
        width 100%
        background-color lightgray
    .imgwr
        max-height 60px
        max-width 30%
    img
        object-fit contain
        width 100%
        height 100%
</style>