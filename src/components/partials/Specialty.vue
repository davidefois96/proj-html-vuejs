<script>
  export default {
    props:{

      name:String,
      color:String


    }
    
  }
</script>

<template>
  <div class="text-white px-2 py-5" :style="`background-color: ${color}`">
    <h6>{{ name }}</h6>
    <img class="my-3" src="/img/wave-divider.png" alt="wave-divider">
    <p class=" lh-lg mb-3">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudatium, totam rem aperiam, eaque</p>
    <button>LEARN MORE</button>


  </div>
</template>



<style lang="scss" scoped>



 

 button{

    font-size: 0.8rem;
    background-color: transparent;
    border-radius: 0%;
    padding-left: 15px;
    padding-right: 15px;
    padding-top: 5px;
    padding-bottom: 5px;
    border:solid white 1px;
    color: white;


  }
  p{
    font-size: 0.8rem;
    text-align: center;
   
  }

</style>