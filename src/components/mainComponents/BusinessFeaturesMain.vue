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
      <div class="row">
        <div class="col">
          <h2>Popular features that your business needs</h2>
          <p>Faff about only a quid blower i don't want no agro bleeding chimney pot burke tosser cras nice one boot fanny.!</p>
        </div>
        <div class="col">
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
.mc-card{
  width: 260px;
  height: 160px;
}
</style>