<template>
    <div @start="start" @stop="stop">
         
            <CarouselSlide v-for="(slide, index) in info" :key="index" :index="index" :visibleimg="visibleImg" :srcp='slide.url' :direction="direction">
            <!-- <CarouselSlide v-for="(slide, index) in info" :key="index"> -->
                               
            </CarouselSlide>
      <div class="dots">
        <span v-for="(slide, index) in info" :key="index" class="dot" :class="{ active: index === visibleImg }"></span>
      </div>
    </div>
</template>

<script>
// import Carousel from './carousel';
import CarouselSlide from './carouselSlide';

export default{
    name: 'SlideShow',
    props: ['info'],
    components: { CarouselSlide},
 
    data(){
        return {
            visibleImg: 0,
            direction: 'left',
            interval: null,

        }
    },
    methods:{
        next() {
            if (this.visibleImg == this.info.length - 1)
                this.visibleImg = 0 ;
            else
                this.visibleImg++;
            this.direction = 'right';
        },
        start() {
            this.interval = setInterval(this.next, 3000);
            // keu len ham next o tren
        },
        stop() {
            clearInterval(this.interval);
        },
    },
    mounted() { 
        this.start();
    },
    beforeUnmount() {
        this.stop();
    }
}
</script>

<style lang="stylus" scoped>
  
    .dots
        position: absolute
        bottom: 20px
        left: 50%
        transform: translateX(-50%)
        display: flex
        justify-content: center
        gap: 10px

    .dot
        width: 10px
        height: 10px
        background-color: rgba(255, 255, 255, 0.5)
        border-radius: 50%
        cursor: pointer

    &.active
        background-color: orange
    .sliderow
        display flex
        flex-direction column
        overflow hidden
        justify-content center
    .left-enter-active {
        animation: leftAnimation 1s ease-in-out;
    }
    .left-leave-active{
        animation: leftOutAnimation 1s ease-in-out;
    }
    @keyframes leftAnimation {
        from {transform: translateX(100%);}
        to { transform: translateX(0);}
    }
    @keyframes leftOutAnimation{
        from {transform: translateX(0);}
        to {transform: translateX(-100%);}
    }
    
    .right-enter-active {
        animation: rightAnimation 1s ease-in-out;
    }
    .right-leave-active{
        animation: rightOutAnimation 1s ease-in-out;
    }
    @keyframes rightAnimation {
        from {transform: translateX(-100%);}
        to { transform: translateX(0);}
    }
    @keyframes rightOutAnimation{
        from {transform: translateX(0); }
        to {transform: translateX(100%);}
    }
    .imgcontainer {
        width: 200px;
        height: 250px;
    }
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
</style>