<script>
  export default {
    
    props:{

      service:Object


    }
  }
</script>


<template>
  <div>

    
    <img :src="`/img/${service.img}`" alt="">

    
    
    <h3 class="mt-2">{{service.name}} </h3>

    <div class="line my-4  "></div>

    <p class="lh-lg ">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium <br> doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo <br> inventore veritatis et quasi architecto beatae</p>

  </div>
</template>



<style lang="scss" scoped>


.line{
  border: 1px solid black;
  width: 200px;
  margin: auto;


}
</style>