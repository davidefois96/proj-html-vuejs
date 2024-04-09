<script>
import Cardscontainer from './partials/Cardscontainer.vue'


  export default {
    
    components:{
      Cardscontainer

    }
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

      <Cardscontainer />


    </section>

  </main>
</template>



<style lang="scss" scoped>


main{

  
  .firstSection{

    padding-top: 90px;
    padding-bottom: 90px;



  }
  
}
</style>