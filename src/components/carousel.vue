<template>
        <div class="imgcontainer">
            <slot></slot>
        </div>

        <!-- <button @click="next" class="next">Next</button> -->
        <!-- <button @click="prev" class="prev">Prev</button> -->

       
</template>

<script>
export default {
    name: 'CarouselWrapper',
    methods: {
        next() {
            this.$emit('next');
        },
        prev() {
            this.$emit('prev');
        }
    }
}
</script>

<style scoped lang='stylus'>
   .imgcontainer
        position: relative
        // this is for the child component to be absolute in relation to this parent
        width: 100%
        overflow: hidden
        // background-color: blue

    button
        position: absolute
        top: 50%

    .prev
        left: 0

    .next
        right: 0

  

   
</style>