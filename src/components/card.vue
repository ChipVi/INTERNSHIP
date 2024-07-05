<template >
    <div class="cards">
        <div v-for="(each, i) in info" :key="i">
            <div class="card">
                <div class="imgcontainer">
                    <img :src='each.url' alt="">
                </div>
                <div class="ten"> {{ each.ten }} </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'user-card-component',
  props: ['info'],
};
</script>

<style scoped>
.cards {
    display: flex;
    flex-direction: row;
    overflow-x: scroll;
    scroll-snap-type: x mandatory;
    width:100%;
    background-color: white;
}
::-webkit-scrollbar {
    display: none;
}
.card{
    display:flex;
    flex-direction: column;
    padding: 5px;
    width: 5rem;
    border-radius: 6px;
    scroll-snap-align: start;
    transition: all 0.2s;
    margin: 0 5px;
}
.imgcontainer{
    width: 100%;
    height: 80%;
    
}
img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 6px;
}
.ten{
    font-size: 12px;
    overflow: hidden;
}
</style>