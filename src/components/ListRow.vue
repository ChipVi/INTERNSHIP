<template lang="pug">
.book-card
  .book-image
    img(src="../assets/doc3.jpg" alt="Book Cover")
  .book-details
    .book-title Đệ Nhất Thứ Ma Pháp Thế
    .book-author Charlotte · Mecklen xuyên qua đến Fars đế quốc, chỉ muốn làm cái dị đại lục...
    //- star(:rating='info.rate')
</template>

<script>
// import star from './star.vue';
export default {
  name: 'star',
  components: {
    // star
  },
  props: ['info']
};
</script>

<style lang="stylus" scoped>
        img 
          max-height 100%
          max-width 100%
          object-fit contain
        .book-card {
            display: flex;
            align-items: center;
            padding 10px;
            max-width: 400px;
            max-height: 200px;
            background-color white
            margin-bottom: 10px
        }
        
        .book-image {
            max-width: 100px;
            max-height: 130px;
            margin: 0 10px ;
        }
        .book-details {
            flex-grow: 1;
        }
        .book-title {
            font-size: 16px;
            font-weight: bold;
            padding 0
            margin 0
        }
        .book-author {
            font-size: 13px;
            color: gray;
        }
</style>