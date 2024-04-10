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
    <a href=""><p>{{text}}</p></a>


  </li>
</template>



<style lang="scss" scoped>

a{color:#2b2b2b}




.circle{
  width:22px;
  height: 22px;
  border-radius: 50%;
  background-color: aqua;
  text-align: center;
  line-height: 18px;


}

</style>