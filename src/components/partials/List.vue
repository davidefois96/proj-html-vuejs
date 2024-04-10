<script>


  export default {

    props:{
      color:String,
      bg:String,
      text:String,
      icon:String,
      iconsize:String

    }
    
  }
</script>

<template>
  <li class="d-flex mb-2 ">

    <div class="circle me-2 " :style="`background-color: ${bg}; color: ${color};`"><i :class="`${icon}`" :style="`font-size: ${iconsize};`"></i></div>
    <p>{{text}}</p>


  </li>
</template>



<style lang="scss" scoped>

@use '../../assets/scss/partials/variables.scss' as *;


.circle{
  width:22px;
  height: 22px;
  border-radius: 50%;
  background-color: aqua;
  text-align: center;
  line-height: 18px;


}

</style>