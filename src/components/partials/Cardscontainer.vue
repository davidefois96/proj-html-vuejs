<script>
import Minicard from './Minicard.vue';

import {database} from '../../assets/data/database';

  export default {
    
    components:{
      Minicard


    },
    data() {
      return {
        database
      }
    },
  }
</script>

<template>
  <div class="customContainer row row-cols-4 text-center" >
    <Minicard v-for="(characteristic, index) in database.characteristics" :key="index"
      :img="characteristic.img"
      :name="characteristic.name"
    />
    

  </div>
</template>



<style lang="scss" scoped>
@use '../../assets/scss/partials/variables.scss' as *;

</style>