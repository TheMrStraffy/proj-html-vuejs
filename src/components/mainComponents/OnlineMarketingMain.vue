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

    <div class="row ">

      <div
      v-for="(item, index) in store.info" :key="index"
       class="col">

        <div class="row">
          <div class="col">
            <img :src=" getPathImage(item.image) " alt="">
          </div>
          <div class="col">
            <h4>{{item.title}}</h4>
            <p>{{item.detail}}</p>
            <ul>
              <li 
              v-for="(listItem, index) in item.list" :key="index"
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
</style>