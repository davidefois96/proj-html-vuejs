<script>
  export default {
    
  }
</script>

<template>
  <footer >
    <div class="customContainerBig d-flex align-items-center  position-relative ">

      <p> &#169 Copyright 2012-2020 | Avada Theme by Theme Fusion | All Rights Reserved | Powered by Wordpress</p>
      <div class="box"><i class="fa-solid fa-chevron-up"></i></div>


    </div>

  </footer>
</template>



<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;

footer{
  height:60px;
  background-color: #f7f7f7;
  font-size: 0.76rem;
  .customContainerBig{
    height: 100%;
  }
  .box{
    height:25px;
    width: 35px;
    background-color: #474747;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
    position: absolute;
    bottom: 0;
    right: 0;
    color: white;
    text-align: center;
    line-height: 25px;
    
  }

}

</style>