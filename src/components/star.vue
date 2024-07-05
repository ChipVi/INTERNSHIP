<template lang="pug">
    .bar
        span.fa.fa-star.checked(v-for="star in rating" :key='star')
        span.fa.fa-star.checked(v-for="star in starsLeft" :key='star' class='star')
        
        
</template>

<script>
export default {
    name: 'footer',
    props:['rating'],
    computed:{
        starsLeft() {
            return 5 - this.rating;
        }
    }

}
</script>

<style lang="stylus" scoped>
    span
        color: #F4BB44
    .star
        color: #FFDEAD

</style>