<template lang="pug">
.card.text-center
    .mt-4
        img(src="@/assets/doc3.jpg" alt="Card image cap").img-thumbnail.img-fluid
    .card-body.p-0
        h5.mt-2 Special title treatment
        h6 Nguyen Khanh Vi
        p.m-0
            strong 530 chuong 
        p.m-0
            em lorem ipsum lorem ipsom...
</template>
<script>
export default {
    name: 'box',
    data() {},
    components: [],
}
</script>

<style lang="stylus" scoped>
// .imgw
//     width 80%
//     height 50%
    
img 
    object-fit: full
    max-width: 100%
    max-height 100%
.card
    width 100%
    display flex
    align-items center
</style>