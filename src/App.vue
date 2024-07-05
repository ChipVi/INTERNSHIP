<template lang='pug'>
.app
    Header
    slide
    Toolbar

    .tieude
      .title TRUYỆN MỚI CẬP NHẬT
      .xemthem >
    SwitchButton(:info='info')

    .tieude
      .title TRUYỆN XEM NHIỀU
      .xemthem >
    card(:info='info')

    .tieude
      .title TRUYỆN ĐỀ CỬ THÁNG
      .xemthem >
    ListRow(:info='info')

    .tieude
      .title TRUYỆN ĐÃ HOÀN THÀNH
      .xemthem >
    ListRow(:info='info')

    Footer
</template>

<script>
import slide from './components/slide'
import Header from "./components/header";
import Toolbar from './components/ToolBar';
import SlideShow from './components/SlideShow';
import SwitchButton from './components/SwitchButton';
import ListRow from './components/ListRow';
import Footer from './components/Footer';
import card from './components/card';
export default {
  name: 'App',
  components: {
    SlideShow,
    Header,
    Toolbar,
    SwitchButton,
    ListRow,
    Footer,
    card,
    slide,
  },
  data() {
    return {
     
      info: [{
        ten: 'Conan tham tu lung danh',
        url: 'https://picsum.photos/id/237/200/150',
        rate: 2,
        type: 1,
      },
      {
        ten: 'Sakura Thu linh the bai',
        url: 'https://picsum.photos/id/234/200/150',
        rate: 3,
        type: 2,

      },
      {
        ten: 'HarryPotter',
        url: 'https://picsum.photos/id/232/200/150',
        rate: 1,
        type: 1,

      },
      {
        ten: 'Alibaba va 12 ten cuop',
        url: 'https://picsum.photos/id/231/200/150',
        rate: 3,
        type: 0,

      },
      {
        ten: 'Chu cho ngoc nghech',
        url: 'https://picsum.photos/id/230/200/150',
        rate: 5,
        type: 0,

      }
    ],
      
    }
  },
  
}
</script>

<style>

#app {
  background-color: #add8dc;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0 auto;
}

.tieude{
  display:flex;
  justify-content: space-between;
  background-color: white;
  padding: 10px 0px;
  margin: 20px 0 0;
  font-weight: bold;

}

</style>
