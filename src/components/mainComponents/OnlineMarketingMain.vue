<script>
import store from '../../data/store';
export default {
  name: "OnlineMarketingMain",
  components: {
    
  },
  data(){
    return{
      store,
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

    <div class="row " id="aboutUs">

      <div
      v-for="(item, index) in store.info" :key="index"
       class="col-12 col-lg-4">

        <div class="row">
          <div class="col-4  text-center">
            <img :src=" getPathImage(item.image) " alt="">
          </div>
          <div class="col-8 ">
            <h4>{{item.title}}</h4>
            <p>{{item.detail}}</p>
            <ul>
              <li 
              v-for="(listItem, index) in item.list" :key="index"
              class="mb-3"
              >
                <i class="fa-solid fa-check"></i>
                {{listItem.info}}
              </li>
            </ul>
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
img{
  display: inline-block;
}
p{
  color: #8E989F;
}
i{
  color: #377DFF;
  margin-right: 8px;
}
</style>