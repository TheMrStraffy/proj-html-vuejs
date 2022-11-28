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
    <div class="wave-box">
    <div class="wave"></div>
    <div class="after-wave"></div>
    </div>
    <div class="row text-area">
      <div class="col text-center" id="testimonials">
        <h2>Our Testimonials</h2>
        <p>If you are planning on developing a product landing app or website,    take a look at this beautiful-crafted</p>
      </div>
    </div>
  <div class="container">

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
    <div class="backgroundImage"></div>

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
  </div>
  </section>
</template>


<style lang="scss" scoped>
section{
  position: relative;
}
.wave-box{
  position: absolute;
  top: -120px;
  left: 0;
  width: 100%;
  .wave{
  
    width: 100%;
    height: 280px;
    background-image: url('../../assets/img/15.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: -50px;
    filter: opacity(0.05);
    background-color: black;
  }
  .after-wave{
  width: 100%;
      height: 50px;
      background: linear-gradient(#F2F2F2, white);
  }
}
section{
  margin-bottom: 110px;
  .text-area{
    margin-bottom: 110px;
  }
}
h2{
  margin-bottom: 30px
}
p, span{
  color: #8e989f;
}
.backgroundImage{
  position: fixed;
  z-index: -1;
  top: 0;
  left: 0;
  width: 100%;
  height: 200px;
  margin-top: 50px;
  filter:opacity(0.05);
  background-image: url('../../assets/img/comma.png');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
 }
.mc-card{
  width: 500px;
  height: 350px;
  margin-bottom: 50px;
  // add box-shadow
 box-shadow: 0px 50px 0px 26px rgba(119, 119, 119, 0), 0px 5px 0px 0px rgba(148, 148, 148, 0.7), 0px 15px 0px -5px rgba(156, 156, 156, 0.6), 0px 25px 0px -10px rgba(209, 209, 209, 0.59);
 
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