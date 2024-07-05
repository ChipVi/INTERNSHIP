<template lang="pug">
    .footer
        .icon
            span Android
            span iOS
            span PC 
        p Copyright (c) 2014 Thunderagon Development Team
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
    .footer 
        display flex
        flex-direction column
        align-items center
        background-color white 
</style>