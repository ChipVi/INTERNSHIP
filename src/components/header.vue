<template>
    <div class="header">
        <h3>
            TÀNG THƯ VIỆN
        </h3>
        <div class="menu">
            <div v-if="isLargeScreen" class="large-screen-content">
                    <input type="text" placeholder="Tìm tên truyện hoặc tác giả">
            </div>
            <ul>
                <li><a href="#"><i class="fas fa-search"></i></a></li>
                <li><a href="#"><i class="fas fa-user-alt"></i></a></li>
                <li><a href="#"><i class="fas fa-users"></i></a></li>
            </ul>
        </div>
     
    </div>
</template>
<script>
    export default {
    name: 'header',
    data() {
    return {
      screenWidth: window.innerWidth
    };
  },
    computed: {
        isLargeScreen() {
            return this.screenWidth >= 1024; // Adjust the breakpoint as needed
        }
    },
    created() {
    window.addEventListener('resize', this.updateScreenWidth);
    },
    beforeUnmount() {
        window.removeEventListener('resize', this.updateScreenWidth);
    },
    methods: {
        updateScreenWidth() {
        this.screenWidth = window.innerWidth;
    }
  }
}
    
</script>
<style scoped>
    .menu{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    @media (min-width: 1024px) {
    .large-screen-content {
    }
    }
    .header{
        display: flex;
        justify-content:space-between;
        align-items: center;
        background-color: #2798a1;
        padding: 0 10px;
        color: white;
    }
    ul{
        list-style-type: none;
        display:flex;
        padding: 10;
    }
    a {
            color: inherit; /* This will inherit the color from its parent */
            text-decoration: none; /* Optional: Remove underline */
    }
    a:hover{
        color: pink;
    }
    i{
        font-size: 25px;
    }
    li{
        margin: 10px;
    }
    

</style>