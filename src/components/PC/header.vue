<template lang="pug">
.header
        .logo 
            .img(src="#")
        .searchbar 
            input(type="text" placeholder="Search..")
            a(href="#")
                i.fas.fa-search
        .logout 
            a(href="#")
                i.fa.fa-sign-out

</template>
<script>
    export default {
        name: 'header'
    }
</script>
<style scoped>
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