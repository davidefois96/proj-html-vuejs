<script>
import { database } from '../assets/data/database';
  export default {
    data() {
      return {
        database
      }
    },
    
    
  }
</script>

<template>
  <header >
    <div class="customContainerBig topHeader d-flex justify-content-between pt-4">

      <img src="/img/medical_logo_1x_light.png" alt="">

      <ul class="d-flex align-items-center ">

        <li v-for="(item,index) in database.headerlist" :key="index"><a href="" :style="`color: ${item.color} ;`">{{ item.name }}</a></li>
        
        <li>
          
          <button>MAKE APPOINTMENT</button>
        
        </li>
      </ul>


    </div>

    <div class="customContainer d-flex">

      <div>
        <h1>Caring <span>For Life</span></h1>
        <p class="my-4 lh-lg ">Kind words can be short and easy to speak, but their echoes are truly <br>
        endless. Avada Healt focuses on you as if it was our own family.
        </p>
        <button>LEARN MORE</button>


      </div>

      
    </div>

    

  </header>
</template>



<style lang="scss" scoped>



header{
  background-image: url(/img/header-image-homepage.jpg);
  
  background-position: top;
  height: 850px;

  
  .topHeader{
    
    img{
      width: 15%;
      
    }

  }
  
  ul{
    
    list-style: none;
    text-decoration: none;
    font-size: 0.8rem;
   

    
    li{
      margin-left: 40px;

      button{
        font-size: 0.8rem;
        color: white;
        background-color: #39afbb;
        border-radius: 0%;
        padding-left: 30px;
        padding-right: 30px;
        padding-top: 6px;
        padding-bottom: 6px;
        border: none;


      }

    }


  }

  
  .customContainer{
    height: 660.8px;
    padding-top: 220px;
    color: white;

    
    h1{
      font-size: 4rem;
      
      span{color: #39afbb}

    }
    button{
        font-size: 0.9rem;
        color: white;
        background-color: #39afbb;
        border-radius: 0%;
        padding-left: 58px;
        padding-right: 58px;
        padding-top: 10px;
        padding-bottom: 10px;
        border: none;
        


      }



  }
}
</style>