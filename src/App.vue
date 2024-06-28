<template lang="pug">
#app
  .head 
    div
      h3 Tàng thư viện

  Slider
  a(href="http://")
    div.link Tải app ngay
  div.danhmuc Truyện mới nhất
  div.slide
    Carddung(v-for="card in truyen"
      :avatar='card.avatar'
      :tentruyen='card.tentruyen'
    )
    
  a(href="http://")
    div.link Tải app ngay

  div.danhmuc Truyện xem nhiều
  div.col(v-for="card in truyen")
    UserCard(
      :avatar='card.avatar'
      :tentruyen='card.tentruyen'
      :theloai='card.theloai'
      :tinhtrang='card.tinhtrang'
      :sochuong='card.sochuong'
      )
</template>

<script>
import UserCard from './components/cardngang.vue';
import Carddung from './components/carddung.vue';
import Slider from './components/slider.vue';

export default {
  name: 'App',
  components: {
    UserCard, Slider, Carddung
  },
  data() {
    return {
      translatevalue: 0,
      truyen: [
        {
          avatar: 'https://picsum.photos/200/300',
          tentruyen: 'One Piece',
          theloai: 'Adventure',
          tinhtrang: 'Đã hoàn thành',
          sochuong: 100
        },
        {
          avatar: 'https://picsum.photos/200/300',
          tentruyen: 'Sakura',
          theloai: 'Adventure',
          tinhtrang: 'Chua hoàn thành',
          sochuong: 50
        },
        {
          avatar: 'https://picsum.photos/200/300',
          tentruyen: '3',
          theloai: 'Adventure',
          tinhtrang: 'Đã hoàn thành',
          sochuong: 100
        },
        {
          avatar: 'https://picsum.photos/200/300',
          tentruyen: '4',
          theloai: 'Adventure',
          tinhtrang: 'Đã hoàn thành',
          sochuong: 100
        },
        {
          avatar: 'https://picsum.photos/200/300',
          tentruyen: '4',
          theloai: 'Adventure',
          tinhtrang: 'Đã hoàn thành',
          sochuong: 100
        }
      ],
    };
  },
  
};
</script>

<style lang="stylus">
body
  background-color: silver
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  margin 0 auto
  .head
    background-color: white
    height 20%
    width 100%
  .col
    width 100%
  .slide
    width 100%
    height 30%
    display flex
    overflow hidden
    transform translate3d(' + translatevalue + 'px, 0px, 0px)
  
  .link
    background-color linen
  .danhmuc
    background-color: white
 
</style>