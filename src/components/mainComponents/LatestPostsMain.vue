<script>
import store from '../../data/store';
export default {
  name: "LatestPostsMain",
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
    <div class="row text-center text-area">

    <h2>Latest Posts</h2>
    <p>If you are planning on developing a product landing.</p>
    </div>
    <div class="row justify-content-between">
      <div 
      v-for="(post, index) in store.latestPosts" :key="index"
      class="col-3">
        <div class="mc-card">
          <div class="img-box">
            <span>{{post.date}}</span>
            <img :src="getPathImage(post.image)" alt="">
          </div>
          <h4>{{post.title}}</h4>
          <p>{{post.description}}</p>
        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
.text-area{
  margin-bottom: 100px;
}
.mc-card{
  width: 350px;
  height: 400px;
  .img-box{
    position: relative;
    width: 325px;
    height: 215px;
    span{
      position: absolute;
    }
    img{
      height: 100%;
      width: 100%;
    }
  }
}
</style>