<script>
  export default {
    
    props:{
      img:String,
      name:String,
      type:String



    }
  }
</script>

<template>

  <div class="mt-5">
   <img :src="`/img/${img}`" :alt="`${name}`">
   <div class="bg-white  text-start p-4 lh-lg ">
    <p class="m-0">{{ name }}</p>
    <p>{{ type }}</p>

    <p class="p1 my-4 ">At vero eos et accusamus et iusto odio <br> dignissimos ducimus qui blanditiis <br> praesentium voluptatum deleniti atque</p>

    
   <div>

    <a class=" btn1 text-white " href="#" role="button"><i class="fa-brands fa-facebook-f"></i></a>
    <a class=" btn2 text-white  mx-1 " href="#" role="button"><i class="fa-brands fa-twitter"></i></a>
    <a class=" btn3 text-white " href="#" role="button"><i class="fa-brands fa-instagram"></i></a>



   </div>




    
      
    

    


   </div>
 </div>

</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/variables.scss' as *;

img{

  width: 100%;
}

p{
  font-size: 0.9rem;


}
.p1{

  font-size: 0.78rem;
}

.btn1{
  background-color: $facebook;


}
.btn2{
  background-color: $twitter;


}
.btn3{
  background-color: $instagram;


}
a{
  display: inline-block;
  height: 25px;
  width:25px;
  font-size: smaller;
  text-align: center;
  line-height: 25px;
  border-radius: 3px;
}

</style>