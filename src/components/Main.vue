<script>
import Skill from './partials/Skill.vue';
import Service from './partials/Service.vue';
import Card from './partials/Card.vue';
import Specialty from './partials/Specialty.vue';

import { database } from '../assets/data/database';

  export default {
    
    components:{
      Skill,
      Service,
      Card,
      Specialty

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

    <section class="fifthSection row row-cols-3">

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

  </main>
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/variables.scss' as *;


main{

  
  .firstSection{

    padding-top: 90px;
    padding-bottom: 90px;
    text-align: center;



  }
  .secondSection{

    padding-top: 90px;
    padding-bottom: 90px;
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
        background-color: $pelorous;
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
        }

      }
    }
    

  }
  
}
</style>