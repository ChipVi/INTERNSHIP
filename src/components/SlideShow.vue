<template>
    <div @mouseenter="stop" @mouseleave="start" class="wrap-caroucel">
      <CarouselSlide
        v-for="(slide, index) in info"
        :key="index"
        :index="index"
        :visibleimg="visibleImg"
        :srcp="slide.url"
        :direction="direction"
      />
      <div class="dots">
        <span
          v-for="(slide, index) in info"
          :key="index"
          class="dot"
          :class="{ active: index === visibleImg }"
          @click="goToSlide(index)"
        ></span>
      </div>
    </div>
  </template>
  
  <script>
  import CarouselSlide from './carouselSlide';
  
  export default {
    name: 'SlideShow',
    props: ['info'],
    components: { CarouselSlide },
    data() {
      return {
        visibleImg: 0,
        direction: 'left',
        interval: null,
      };
    },
    methods: {
      next() {
        this.direction = 'right';
        this.visibleImg = (this.visibleImg + 1) % this.info.length;
      },
      start() {
        this.stop(); // Dừng trước khi bắt đầu mới để tránh nhiều interval chạy cùng lúc
        this.interval = setInterval(this.next, 3000);
      },
      stop() {
        if (this.interval) {
          clearInterval(this.interval);
          this.interval = null;
        }
      },
      goToSlide(index) {
        this.direction = index > this.visibleImg ? 'right' : 'left';
        this.visibleImg = index;
      },
    },
    mounted() {
      this.start();
    },
    beforeUnmount() {
      this.stop();
    },
  };
  </script>
  
  <style lang="stylus" scoped>
  .wrap-caroucel {
    height: 12rem;
    overflow: hidden;
    position: relative;
    display: flex;
  }
  .dots {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    justify-content: center;
    gap: 10px;
  }
  .dot {
    width: 10px;
    height: 10px;
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 50%;
    cursor: pointer;
  }
  .dot.active {
    background-color: orange;
  }
  </style>