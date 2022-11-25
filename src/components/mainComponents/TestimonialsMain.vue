<script>
import store from '../../data/store';
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
import { Pagination, Navigation } from "swiper";
export default {
  name: "TestimonialsMain",
  components: {
    Swiper,
    SwiperSlide,
  },
  methods:{
    getPathImage(imageName){
      return new URL(`../../assets/img/${imageName}`,
      import.meta.url).href
    }
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      store
    };
  },
  
}
</script>
<template>
  <section>
    <div class="row text-area">
      <div class="col text-center">
        <h2>Our Testimonials</h2>
        <p>If you are planning on developing a product landing app or website,    take a look at this beautiful-crafted</p>
      </div>
    </div>

    <swiper 
    :slidesPerView="2"
    :spaceBetween="30"
    :slidesPerGroup="2"
    :loop="true"
    :loopFillGroupWithBlank="true"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide
    v-for="(person, index) in store.testimonials" :key="index"
    class="mc-card"
    >
      <div class="row h-100">
        <div class="col h-100 d-flex flex-column justify-content-center text-center">
          <div class="img-box">
            <img :src="getPathImage(person.image)" :alt="person.name">
          </div>
          <h4>{{person.name}} <span>- {{person.position}}</span></h4>
          <p>{{person.description}}</p>
        </div>
      </div>
    </swiper-slide>

    

  </swiper>
  </section>
</template>


<style lang="scss" scoped>
section{
  margin-bottom: 110px;
  .text-area{
    margin-bottom: 110px;
  }
}
h2{
  margin-bottom: 30px
}

.mc-card{
  width: 500px;
  height: 350px;
  margin-bottom: 50px;
  // add box-shadow
  h4{
    margin-bottom: 35px;
  }
  p{
    margin-bottom: 45px;
  }
}
.img-box{
  align-self: center;
  margin: 50px 0;
  width: 65px;
  height: 65px;
  
  img{
    width: 100%;
    height: 100%;
    border-radius: 50%;
  }
}
</style>