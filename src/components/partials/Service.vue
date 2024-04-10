<script>
  export default {
    
    props:{

      service:Object


    }
  }
</script>


<template>
  <div>

    
    <img class="mb-2" :src="`/img/${service.img}`" alt="">

    
    
    <h3 :style="`color: ${service.color}`" >{{service.name}} </h3>

    <div class="line my-4  "></div>

    <p class="lh-lg " :style="`color: ${service.color}`">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

  </div>
</template>



<style lang="scss" scoped>




.line{
  border: 1.2px solid #d1d1d1;
  width: 200px;
  margin: auto;


}




</style>