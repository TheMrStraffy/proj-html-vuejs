<script>
import store from "../../data/store";
export default {
  name: "BusinessFeaturesMain",
  data(){
    return{
      store
    }
  },
  methods:{
    getPathImage(imageName){
      return new URL(`../../assets/img/${imageName}`,
      import.meta.url).href
    }
  }
}
</script>
<template>
  <section>
    <div class="row">
      <div class="row justify-content-between" id="feature">
        <div class="col-8">
          <h2>Popular features that your business needs</h2>
          <p class="w-75">Faff about only a quid blower i don't want no agro bleeding chimney pot burke tosser cras nice one boot fanny.!</p>
        </div>
        <div class="col-3">
          <div class="btn btn-primary"> Explore More Feature</div>
        </div>
      </div>
      <div class="row justify-content-between">
          <div 
          v-for="(item, index) in store.businessFeatures" :key="index"
          class="mc-card col-3 my-3">
            <h4>{{item.title}}</h4>
            <div class="img-box">
              <img :src="getPathImage(item.img)" :alt="item.title">
            </div>
          </div>
          
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
section{
  margin-bottom: 150px;
}
p{
  color: #8e989f;
}
.mc-card{
  padding: 20px 10px;
  width: 260px;
  height: 160px;
  box-shadow: 0px 0px 60px -30px rgb(177, 177, 177);
  -webkit-box-shadow: 0px 0px 60px -30px rgba(177, 177, 177);
  -moz-box-shadow: 0px 0px 60px -30px rgba(177, 177, 177);
  transition: all 0.5s linear;
  &:hover{
    color: white;
    background-color: #6CDAC1;
  }
}
.img-box{
  height: 40px;
  
  img{
    margin-left: 20px;
    height: 100%;
  }
}
</style>