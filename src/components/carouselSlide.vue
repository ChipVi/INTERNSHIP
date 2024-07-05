<template>
    <!-- if there are name here, the css class would be replaced by name-enter-active instead of v-enter-active -->
    <transition :name="direction" mode="out-in">
        <div class="imgcontainer">
            <img v-if="visibleimg === index" :src="srcp">
        </div>
    </transition>

</template>

<script>
export default {
    props: ['index', 'visibleimg', 'direction','srcp'],
    data() {
        return {
            
        }
    }
}
</script>

<style scoped>
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