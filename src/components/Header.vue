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
    <div class="topHeader d-flex justify-content-between pt-4">

      <img src="/img/medical_logo_1x_light.png" alt="">

      <ul class="d-flex align-items-center ">
        <li>HOME</li>
        <li>ABOUT</li>
        <li>DEPARTMENTS</li>
        <li>ARTICLES</li>
        <li>
          
          <button>MAKE APPOINTMENT</button>
        
        </li>
      </ul>


    </div>

    <div class="customContainer d-flex">

      <div>
        <h1>Caring <span>For Life</span></h1>
        <p class="my-4">Kind words can be short and easy to speak, but their echoes are truly <br>
        endless. Avada Healt focuses on you as if it was our own family.
        </p>
        <button>LEARN MORE</button>


      </div>

      
    </div>

    

  </header>
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/variables.scss' as *;


header{
  background-image: url(/img/header-image-homepage.jpg);
  background-size: cover;
  height: 730px;

  
  .topHeader{
    padding-left: 100px;
    padding-right: 100px;

    
    img{
      width: 16%;
      height: 16%;

    }

  }
  
  ul{
    color: white;
    list-style: none;
    text-decoration: none;
    font-size: 0.8rem;
   

    
    li{
      margin-left: 50px;
      vertical-align: middle;
      
      &:first-child{color: $pelorous;};
      
      button{
        font-size: 0.8rem;
        color: white;
        background-color: $pelorous;
        border-radius: 0%;
        padding-left: 15px;
        padding-right: 15px;
        padding-top: 5px;
        padding-bottom: 5px;
        border: none;


      }

    }


  }

  
  .customContainer{
    height: 660.8px;
    padding-top: 160px;
    color: $white;

    
    h1{
      font-size: 4rem;
      
      span{color: $pelorous}

    }
    button{
        font-size: 0.8rem;
        color: white;
        background-color: $pelorous;
        border-radius: 0%;
        padding-left: 50px;
        padding-right: 50px;
        padding-top: 10px;
        padding-bottom: 10px;
        border: none;


      }



  }
}
</style>