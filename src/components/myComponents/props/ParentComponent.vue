<script>
import ChildComponent from './ChildComponent.vue';


export default{
    components:{ChildComponent},
    data(){
        return{
            movieTitle:'Shazan',
            brand:"",
            count: 0,
        }
    },
    methods:{
        receivedBrand(data){
            this.brand =data;
            this.count++;
        }
    },
}
</script>
<template>
  <h2>I'm your father</h2>
  <span>{{ movieTitle }}</span>
  <ChildComponent :movieTitle = "movieTitle" @brand="receivedBrand"/>
  <span>BRAND: {{ brand }} /{{count}}</span>
  
</template>
<style scoped></style>
