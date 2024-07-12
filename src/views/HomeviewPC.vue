<template lang="pug">
Header
navbar
.container.text-center
  .row.content
    .col-lg-3.d-none.d-lg-block
        h5.fw-bold.mt-1 Thể loại
        .row(v-for="each in 6" :key="each").p-0.bg-white
                .col-lg-6.col-md-4.col-sm-2
                    typecard
                .col-lg-6.col-md-4.col-sm-2
                    typecard
      
           
    .col-lg-6.text-left
        slide(:info='info')
        .container
            .row.first-row
                .small-box Lấm Uyên Hành
                .small-box Vạn Cổ Tối Cường Tông
                .small-box Lấm Uyên Hành
                .small-box Lấm Uyên Hành
                .small-box Lấm Uyên Hành
            .row.second-row
                a
                    img(src="https://picsum.photos/id/237/1400/1000" alt="Image 1")
                a
                    img(src="https://picsum.photos/id/237/1400/1000" alt="Image 1")
                a
                    img(src="https://picsum.photos/id/237/1400/1000" alt="Image 1")

    .col-sm-6.d-none.d-sm-block.d-lg-none
        h5.fw-bold.mt-1 Thể loại
        .row(v-for="each in 6" :key="each").p-0
                .col-sm-6
                    typecard
                .col-sm-6
                    typecard
    .col-lg-3.col-sm-6
        news

.container
  .row.content
    .col-lg-3.d-none.d-lg-block
        listdoc

    .col-lg-6.text-left 
        .banner
            .smslide 
                slide(:info='info') 
            .card-body.px-3
                h5.card-title Tên truyện
                p.card-text With supporting text below as a natural lead-in to additional content.
                a.btn.btn-primary(href="#") Đọc ngay
        .hang1
            truyennoibat
            truyennoibat
            truyennoibat
        .hang1
            truyennoibat
            truyennoibat
            truyennoibat
    .col-sm-6.d-none.d-sm-block.d-lg-none
        listdoc
    .col-sm-6.col-lg-3
        listdoc

.container
    title2
    .row
        .col-sm-6.col-lg-3
            carddoc
        .col-sm-6.col-lg-9
            .row(v-for="each in 3" key="each").p-0
                .col-lg-4.col-sm-12
                    listrow(:info='info') 
                .col-lg-4.d-none.d-lg-block
                    listrow(:info='info')
                .col-lg-4.d-none.d-lg-block
                    listrow(:info='info')     
        
.container
    .row
        .col-xl-3.col-sm-6
            title2
            ranking
        .col-xl-3.col-sm-6
            title2
            ranking
        .col-xl-3.col-sm-6
            title2
            ranking
        .col-xl-3.col-sm-6
            title2
            ranking

Footer
</template>
<script>
import news from '../components/PC/tintuc.vue';
import typecard from '../components/PC/theloaicard.vue';
import slide from '../components/SlideShow';
import listdoc from '../components/PC/listdoc.vue';
import truyennoibat from '../components/PC/truyenoibat.vue';
import listrow from '../components/ListRow.vue';
import carddoc from '@/components/PC/carddoc.vue';
import ranking from '@/components/PC/ranking.vue';
import title2 from '@/components/Title.vue';
import Footer from '@/components/Footer.vue';
import Header from '@/components/header.vue';
import navbar from '@/components/PC/navbar.vue';
export default {
    name: 'HomePC',
    components: {
        Header,
        navbar,
        news,
        typecard,
        slide,
        listdoc,
        truyennoibat,
        listrow,
        carddoc,
        ranking,
        title2,
        Footer
    },
    data() {
    return {
     
      info: [{
        ten: 'Conan tham tu lung danh',
        url: 'https://picsum.photos/id/237/1200/800',
        rate: 2,
        type: 1,
      },
      {
        ten: 'Sakura Thu linh the bai',
        url: 'https://picsum.photos/id/234/1200/800',
        rate: 3,
        type: 2,

      },
      {
        ten: 'HarryPotter',
        url: 'https://picsum.photos/id/232/1200/800',
        rate: 1,
        type: 1,

      },
      {
        ten: 'Alibaba va 12 ten cuop',
        url: 'https://picsum.photos/id/231/1200/800',
        rate: 3,
        type: 0,

      },
      {
        ten: 'Chu cho ngoc nghech',
        url: 'https://picsum.photos/id/230/1200/800',
        rate: 5,
        type: 0,

      }
    ],
      
    }
  },
}
</script>
<style lang="stylus" scoped>

.smslide
    width 30%
    height 33.3%
.container
    width 100%
    background-color lightpink
    margin 2rem auto
.sidenav
.banner
    display: flex;
    flex-direction row
    background-color white
    align-items center
    padding-left 1rem
.hang1
    display: flex;
    flex-direction row
    padding 0
.row1{
    display: flex;
    flex-direction row
    justify-content space-around;
    background-color white
    padding 0
    height 14.28%
}

.first-row .small-box {
    flex: 1;
    height: 20%;
    background-color: white ;
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    font-size: 1em;
}

.second-row {
    height: 80%;
    background-color: white ;
    display: flex;
    flex-direction: row;
    align-items: center;
}
a
    display: inline-block
    padding 0
    flex 1
img {
    max-height: 100%;
    max-width: 100%;
    object-fit: contain;
}

</style>