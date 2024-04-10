<script>
import { database } from '../../assets/data/database';

  export default {
   
    
    props:{
      img:String,
      name:String,
      text:String

    },
    data() {
      return {
        database
      }
    },
   
  }
</script>

<template>
  

  <div class="skillcard">
    <img :src="`/img/${img}`" alt="logo"> 
    <h6>{{name}}</h6>
    
    <p class="lh-lg">{{ text }}</p>


  </div>
  
 

</template>



<style lang="scss" scoped>


.skillcard{
  margin-top: 40px;
  margin-bottom: 10px;

  p{
   font-size: 0.84rem;
   color: #747474;
  
  }
  h6{
    font-size: 0.95rem;
    margin-top: 15px;
    margin-bottom: 15px;
    color: #333c4e;

  }
  img{width: 30%;}

  
}  

</style>








