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
    <div class="row justify-content-between align-items-center">
        <div 
        v-for="(post, index) in store.latestPosts" :key="index"
        class="mc-card col-3">
          <div class="img-box text-center">
            <span>{{post.date}}</span>
            <img :src="getPathImage(post.image)" alt="">
          </div>
          <h4>{{post.title}}</h4>
          <p>{{post.description}}</p>
        </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
.text-area{
  margin-bottom: 100px;
}
p{
  color: #8E989F;
}
.mc-card{
  width: 350px;
  height: 400px;
  border: 1px solid #EFF1FE;
  padding: 10px 5px;
  .img-box{
    position: relative;
    width: 100%;
    height: 215px;
    margin-bottom: 1.3rem;
    span{
      position: absolute;
      top: 5px;
      left: 5px;
      background-color: white;
      color: #8E989F;
      border-radius: 3px;
      padding: 3px 5px;
    }
    img{
      height: 100%;
      width: 100%;
    }
  }
}
</style>