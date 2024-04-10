<script>
import Skill from './partials/Skill.vue';
import Service from './partials/Service.vue';
import Card from './partials/Card.vue';
import Specialty from './partials/Specialty.vue';
import List from './partials/List.vue';

import { database } from '../assets/data/database';

  export default {
    
    components:{
      Skill,
      Service,
      Card,
      Specialty,
      List

    },
    data() {
      return {
        database
      }
    },
  }
</script>

<template>
  <main>
    <section class="firstSection">

      <div>

        <h2 class="mb-4">
          Welcome to Avada Health

        </h2>

        <p class=" lh-lg ">
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br>
          doloremque laudantium, totam rem aperiam, eaque ipsa ab illo

        </p>

      </div>

      <div class="customContainer row row-cols-4" >
        <Skill v-for="(skill, index) in database.skills" :key="index"
        :img="skill.img"
        :name="skill.name"
        :text="skill.text"
         />
    

      </div>

      


    </section>

    <section class="secondSection">

      <Service :key="database.services[0].name"
      :service="database.services[0]"
      
      />

      <div class="row row-cols-3 customContainer">

        <Card v-for="(card,index) in database.doctors" :key="index"
        
        :img="card.img"
        :name="card.name"
        :type="card.type"
        
        />
        
      </div>

    </section>

    <section class="thirdSection">

      <Service :key="database.services[1].name"
      :service="database.services[1]"
      
      />

      <div class="customContainer row row-cols-3 text-center" >
        <Skill v-for="(intervention, index) in database.interventions" :key="index"
        :img="intervention.img"
        :name="intervention.name"
        :text="intervention.text"
         />
    

      </div>





    </section>
    <section class="fourthSection d-flex  justify-content-center  align-items-center ">


      <div>

        <Service :key="database.services[2].name"
         :service="database.services[2]"
      
        />

        <img class="mt-5" src="/img/play-icon.png" alt="play-icon">



      </div>

      




    </section>

    <section class="fifthSection d-flex">

      <Specialty v-for="(specialty,index) in database.specialties" :key="index"
      :name="specialty.name"
      :color="specialty.color"
      
      />

    </section>
    <section class="sixthSection text-white d-flex flex-column  align-items-center justify-content-center ">

      <Service :key="database.services[3].name"
         :service="database.services[3]"
      
      />

      <div class="formbox mt-5 ">

        <div class="d-flex justify-content-between ">

          <input type="text" placeholder="Name*">
          <input type="email" placeholder="Email*">
        
        </div>

        <div class="d-flex justify-content-between ">

          <input type="text" placeholder="Phone Number">

          <div class="date">

            <i class="fa-solid fa-calendar-days"></i>
            <input type="text" placeholder="Appointment Date">


          </div>
          


        </div>

        

        <div class="d-flex flex-column ">

          <textarea class="w-100 bg-transparent" placeholder="How can we help?*"></textarea>

          <button>MAKE AN APPOINTMENT</button>




        </div>

        
      </div>



    </section>
    <section class="seventhSection d-flex  align-items-center  ">


      <div class="customContainer d-flex justify-content-between">

        <img :src="`/img/${icon}`" alt="" v-for="(icon,index) in database.iconsBelow" :key="index">


      </div>


    </section>
    <section class="customContainerBig eighthSection row row-cols-3 ">

      <div class="col col1">

        <img src="/img/medical_logo_1x_dark.png" alt="logo">

        <p class=" my-3">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium dolemue <br>launti totam aperiam, eaque ipsa quae abillo. invente veriatis et quasi architecto beatae <br> luptatem accusantium, remaperiamsiat. Voluptatem accusest etsium doloremque <br>
        Laudaien. Lorem ipsum sits dolores ets unser.</p>

        <div class="line pb-2 "></div>

        <h6 class="mb-5">LEARN MORE ABOUT US</h6>

        <div>
          <a v-for="(icon,index) in database.socials" class=" btn2 text-white me-2" :style="`background-color: ${icon.color} ;`" href="#" role="button" :key="index"><i :class="`${icon.icon}`"></i></a>
          
          <a class="text-white bg-danger " href="#" role="button"><i class="fa-brands fa-youtube"></i></a>

        </div>


      </div>
      <div class="col">

        <h6 class="titlelist"> CONTACT INFORMATION </h6>

        <div class="lineSmall my-4 "></div>

        <ul class=" p-0 ">
          <List v-for="(item,index) in database.informationlist" :key="index"
        :bg="item.bg"
        :color="item.color"
        :text="item.text"
        :icon="item.icon"
        :iconsize="item.iconsize"

        />
          

        </ul>



        
      </div>
      <div class="col">

        

        <h6 class="titlelist"> MEDICAL DEPARTMENTS </h6>

        <div class="lineSmall my-4 "></div>

        <ul class="mb-4 p-0">
          
        <List v-for="(item,index) in database.serviceslist" :key="index"
        :bg="item.bg"
        :color="item.color"
        :text="item.text"
        :icon="item.icon"
        :iconsize="item.iconsize"

        />
          

        </ul>

        <button>VIEW OUR DEPARTMENTS</button>

        


        
        
      </div>


    </section>

  </main>
</template>



<style lang="scss" scoped>




main{

  
  .firstSection{

    padding-top: 90px;
    padding-bottom: 90px;
    text-align: center;

    h2,p{color: #333c4e;}



  }
  .secondSection{

    padding-top: 90px;
    padding-bottom: 120px;
    background-color: #f7f7f7;
    text-align: center;



  }
  .thirdSection{

    padding-top: 90px;
    padding-bottom: 90px;
    
    text-align: center;
    
    
    



  }
  .fourthSection{

    background-image: url(/img/paralax-bg-tour-facilities.jpg);
   
    
    background-size: cover;
    background-position: center;
    
    height: 600px;

    padding-top: 90px;
    padding-bottom: 90px;
    
    text-align: center;

    color: white;

    img{

      width:10%;


    }
    

  }
  .fifthSection{
    height: 290px;
    text-align: center;
  
  }
  
  .sixthSection{

    

    height: 860px;
    background-image: url(/img/make-an-appointment.jpg);
    background-position: center;
    text-align: center;

    .formbox{

      width: 570px;

      input{
        width: 48%;
        margin-bottom: 35px;
        height: 45px;
        background: transparent;
        border: 1px solid white;
        font-size: .75rem;
        color: white;
        padding-left: 8px;
        &:focus{
          outline: none;
        }
        
      }
      textarea{

        border: solid 1px white;
        height: 130px;
        margin-bottom: 35px;
        font-size: .75rem;
        color: white;
        padding-top: 8px;
        padding-left: 8px;
        &:focus{
          outline: none;
        }

      }
      button{

        height: 45px;
        border: none;
        border-radius: 2px;
        background-color: #39afbb;
        color: white;
        font-size: .9rem;


      }
      .date{
        width: 48%;
        border: solid 1px white;
        height: 45px;
        padding-left: 8px;
        input{
          width: 94.7%;
          border: none;


        }
        i{
          font-size: .75rem;
          color: #d1d1d1;
        }

      }
    }
    

  }
  .seventhSection{
    background-image: url(/img/rgb-gradient-bar-for-logo-carrasel.jpg);
    background-size: cover;
    height: 290px;
    img{
      width: 20%;
      
    }

  }
  .eighthSection{

    height: 500px;
    font-size: .8rem;
    padding-top: 80px;

    .col1{
      p{
        line-height: 30px;
        color: #666666;
      }


    }

    .line{
      border-top: solid #e0dede 1px;
    }

    .lineSmall{
      border: solid 1px #39afbb;
      width: 40px;

    }



    h6{
      font-size: .9rem;
      color: #333c4e;
      
    }

    .titlelist{font-size: 1.05rem;}

    a{
      display: inline-block;
      height: 25px;
      width:25px;
      font-size: smaller;
      text-align: center;
      line-height: 25px;
      border-radius: 3px;
      
    }

    button{
        
        font-size: .98rem;
        background-color: white;
        border-radius: 0%;
        padding-left: 60px;
        padding-right: 60px;
        padding-top: 11px;
        padding-bottom: 11px;
        border: solid #333333 1px;
        color: #333333;
        


      }
        


  }
  
}
</style>