<script>
import store from '../data/store';
export default {
  name: "FooterApp",
  data(){
    return{
      store
    }
  }
}
</script>
<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-3">
          <div class="img-box d-flex align-items-center">
            <img src="../assets/img/logo-2.png" alt="">
            <span>SOFBOX</span>
          </div>
          <p>It is a long established fact that a reader will be distracted by the readable content.</p>
          <p>Copyright @ 2018 <a href="#">Sofbox</a></p>
        </div>
        <div 
        v-for="(object, index) in store.footerLinks" :key="index"
        class="col-3">
        <h4>{{object.title}}</h4>
        <ul>
          <li v-for="(listItem,indexOne) in object.menu" :key="indexOne">
            <a href="#">{{listItem.item}}</a>
          </li>
        </ul>
        </div>
        
      </div>
    </div>
    <div class="go-top d-flex justify-content-end align-items-center">
      <div class="button-box d-flex align-items-center justify-content-center">

      <a href="#topPage"><i class="fa-solid fa-chevron-up"></i></a>
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
.img-box{
  width: 50px;
  height: 50px;
  img{
    height: 100%;
    margin-right: 10px;
  }
}
.go-top{
  height: 95px;
}
.button-box{

  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #b2b2b2;
  margin-right: 30px;
  a{
    color: white;
    margin-top: 5px;
    i{
      font-size: 1.5rem;
    }
  }
}
</style>