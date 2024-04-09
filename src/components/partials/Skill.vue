<script>
import { database } from '../../assets/data/database';

  export default {
   
    
    props:{
      img:String,
      name:String

    },
    data() {
      return {
        database
      }
    },
   
  }
</script>

<template>
  

  <div class="minicard">
    <img :src="`/img/${img}`" alt="logo"> 
    <h6>{{name}}</h6>
    
   
    
    
    
    <p>Sed ut perspiciatis unde omnis iste natus error sit voluptam accusantim</p>


  </div>
  
  
    
  
  
  


</template>



<style lang="scss" scoped>


.minicard{
  margin-top: 40px;

  p{
   font-size: 0.78rem;
  
  }
  h6{
    font-size: 0.9rem;
    margin-top: 15px;
    margin-bottom: 15px;

  }

  
}  

</style>





}


