<script>
import HeaderStore from '../data/HeaderStore';
export default {
  name: "HeaderApp",
  data(){
    return{
      HeaderStore,
    }
  }
}
</script>
<template>
  <header class="d-flex justify-content-around align-items-center">
    <div class="logo align-items-center ">
        <img src="../assets/img/logo-2.png" alt="sb-marketing Logo">
    </div>

    <nav class="d-flex align-items-center">
      <ul class="d-flex align-items-center mb-0 flex-wrap">
        <li class="mx-3"
        v-for="(item, index) in HeaderStore.menu" :key="index"
        ><a :href="item.link">{{item.text}}</a></li>
        <li class="mx-3"><a href="#"><i class="fa-solid fa-magnifying-glass"></i></a></li>
        <li class="mx-3"><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
      </ul>
      <button type="button" class="btn btn-primary">Get Started</button>
    </nav>
  </header>
</template>


<style lang="scss" scoped>
header{
  height: 85px;
}
.logo{
  width: 45px;
  height: 50px;
  img{
    height: 100%;
    width: 100%;
  }
}
button{
  width: 125px;
  height: 50px;

}
</style>