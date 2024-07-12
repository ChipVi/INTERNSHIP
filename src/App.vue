<template lang='pug'>
.app
    .d-sm-none.d-xs.block
      Homeview
    .d-none.d-sm-block
      HomeviewPC

</template>

<script>
import Homeview from './views/HomeView';
import HomeviewPC from './views/HomeviewPC.vue';
export default {
  name: 'App',
  components: {
    Homeview,
    HomeviewPC
  },
  data() {
  },
  
}
</script>

<style lang="stylus">

#app {
  background-color: white;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0 auto;
}
</style>
