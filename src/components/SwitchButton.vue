<template>
    <div class="typebar">
        <div class="otype" @click="typeconvert(index)" v-for="(each,index) in typebar" :key="index" 
        :class="{active: colorChange === index}"> {{each}}</div>
    </div>

    <card :info='filterType'></card>
      
        
</template>

<script>
import card from './card'
export default {
    name: 'switch',
    props:['info'],
    data(){
        return{
            typebar:['Convert', 'Trans', 'Ngon tinh'],
            colorChange:0,
        }
        
    },
    components:{card},
    methods: {
        typeconvert(id){
            this.colorChange=id;
        }
    },
    computed:{
        filterType() {
            return this.info.filter(each => each.type === this.colorChange);
        }
    }

}
</script>

<style lang="stylus">
    // @media (min-width: 1024px) 
    //     .typebar{
    //     display: flex;
    //     flex-direction:row;
    //     width: 35rem;
    //     height: 2rem;
    //     background-color: white;
    //     border: #2798a1 solid;
    //     border-radius: 3px;
    //     font-size: 1.2rem;
    //     text-align center;
    //     }
    //     .otype{
    //     text-align: center;
    //     height: 100%;
    //     width: 60%;
    //     background-color:white;
    //     font-weight: bold;
    //     }
    //     .otype.active{
    //     background-color:#2798a1;
    //     color:white;
    //     font-weight: bold;
    //     }
    //     .card
    //         width: 8rem;

        .typebar{
        display: flex;
        flex-direction:row;
        width: 100%;
        height: 20%;
        background-color: white;
        border: #2798a1 solid;
        border-radius: 3px;
        }
        .otype{
        text-align: center;
        height: 100%;
        width: 33%;
        background-color:white;
        font-weight: bold;
        }
        .otype.active{
        background-color:#2798a1;
        color:white;
        font-weight: bold;
        }

   


</style>