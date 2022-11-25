<script>
import store from '../data/store';
export default {
  name: "HeaderApp",
  data(){
    return{
      store,
    }
  }
}
</script>
<template>
  <header id="topPage" class="d-flex justify-content-around align-items-center">
    <div class="logo align-items-center ">
        <img src="../assets/img/logo-2.png" alt="sb-marketing Logo">
    </div>

    <nav class="d-flex align-items-center" >
      <ul @click="filter()" class="d-flex align-items-center mb-0 flex-wrap">
        <li class="mx-3" 
        v-for="(item, index) in store.menu" :key="index"
        
        >
        <a 
        
        :href="item.link">{{item.text}}</a></li>
        <li class="mx-3"><a href="#"><i class="fa-solid fa-magnifying-glass"></i></a></li>
        <li class="mx-3 shopLink" >
          <a  href="#">
            <i class="fa-solid fa-cart-shopping"></i>
          </a>
            <span class="shopItems">0</span>

          </li>
      </ul>
      <button type="button" class="btn btn-primary">Get Started</button>
    </nav>
  </header>
</template>


<style lang="scss" scoped>
.shopLink{
  position: relative;
  .shopItems{
    z-index: -1;
    position: absolute;
    bottom: 13px;
    left: 12px;
    background-color: #377DFF;
    color: white;
    border-radius: 50%;
    width: 18px;
    height: 18px;
    line-height: 18px;
    text-align: center;
  }
}
.active{
  border-bottom: 3px solid #377DFF;
    padding-bottom: 15px;
}
a{
  color: #1e1e1e;
  font-weight: 600;
  &:hover{
    border-bottom: 3px solid #377DFF;
    
    padding-bottom: 15px;
  }
}
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
  margin-left: 33px;

}
</style>