<script>
import { database } from '../../assets/data/database';
  export default {
    
    props:{
      img:String,
      name:String,
      type:String



    },
    data() {
      return {
        database
      }
    },
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

    <a v-for="(icon,index) in database.socials" class=" btn2 text-white me-2" :style="`background-color: ${icon.color} ;`" href="#" role="button" :key="index"><i :class="`${icon.icon}`"></i></a>


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

  font-size: 0.76rem;
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