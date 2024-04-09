<script>
import Skill from './partials/Skill.vue';
import Service from './partials/Service.vue';
import Card from './partials/Card.vue'

import { database } from '../assets/data/database';

  export default {
    
    components:{
      Skill,
      Service,
      Card

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

      <div class="text-center">

        <h2 class="mb-4">
          Welcome to Avada Health

        </h2>

        <p class=" lh-lg ">
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br>
          doloremque laudantium, totam rem aperiam, eaque ipsa ab illo

        </p>

      </div>

      <div class="customContainer row row-cols-4 text-center" >
        <Skill v-for="(skill, index) in database.skills" :key="index"
        :img="skill.img"
        :name="skill.name"
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

  </main>
</template>



<style lang="scss" scoped>

@use '../assets/scss/partials/variables.scss' as *;


main{

  
  .firstSection{

    padding-top: 90px;
    padding-bottom: 90px;



  }
  .secondSection{

    padding-top: 90px;
    padding-bottom: 90px;
    background-color: $gallery;
    text-align: center;



  }
  
}
</style>