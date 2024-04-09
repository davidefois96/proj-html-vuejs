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
  
}
</style>