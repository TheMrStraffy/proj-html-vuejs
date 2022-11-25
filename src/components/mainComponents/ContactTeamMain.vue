<script>
export default {
  name: "ContactTeamMain"
}
</script>
<template>
  <section>
    <div class="row text-center text-area">
    <h2>Contact with our team</h2>
    <p>If you are planning on developing a product landing.</p>
    </div>

  <div class="row">
    <div class="col map d-flex justify-content-end">
      <div class="img-box">
        <div class="row box-address ">
          <div class="col">
          <p class="street">Storey Ave</p>
          <p class="main-address">San Francisco, Califoria 94129</p>
          <a href="#">Visualizza mappa più grande</a>
          </div>
          <div class="col d-flex justify-items-center align-items-center text-center flex-column p-0">
            <div class="cropped-img">
            <img src="../../assets/img/entity11_hdpi.png" alt="">
            </div>
            <p>Indicazioni</p>
          </div>
        </div>
        <img src="../../assets/img/StaticMapService.GetMapIma.png" alt="">
      </div>
    </div>
    <div class="col contact">
      <div class="img-logo">
        
        <img src="../../assets/img/logo-2.png" alt="">
        <span>SOFBOX</span>
      </div>
        <p class="address">9840 Shore St.Fond Du Lac, WI 54935</p>

        <div class="details">
          <p>0 1223 456 789</p>
          <p>mail@softbox.com</p>
        </div>

        <div class="row">
          <div class="col">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-github"></i>
            <i class="fa-brands fa-instagram"></i>
          </div>
        </div>

        <h3>Get in Touch</h3>
        <form>
          <div class="d-flex justify-content-between">

          <div class="form-group yourInput">
          <label for="exampleFormControlInput1"></label>
          <input type="email" class="form-control" id="exampleFormControlInput1"      placeholder="Your Name">
        </div>
          <div class="form-group yourInput">
          <label for="exampleFormControlInput1"></label>
          <input type="email" class="form-control" id="exampleFormControlInput1"      placeholder="Your Email">
        </div>
          </div>
          <div class="form-group">
          <label for="exampleFormControlInput1"></label>
          <input type="email" class="form-control" id="exampleFormControlInput1"      placeholder="Your Subject">
        </div>
        <div class="form-group">
          <label for="exampleFormControlTextarea1"></label>
          <textarea class="form-control" id="exampleFormControlTextarea1" placeholder="Your Message"    rows="5"></textarea>
        </div>

        <div class="btn btn-primary">Send Message</div>
        </form>

    </div>
  </div>
  </section>
</template>


<style lang="scss" scoped>

.text-area{
  margin-bottom: 80px;
  h2{
    margin-bottom: 25px;
  }
}
.img-box{
  position: relative;

  .box-address{
  position: absolute;
  background-color: white;
  margin: 10px 0 0 10px;
  width: 300px;
  height: 85px;
  p,a{
    font-size: 0.7rem;
    margin-bottom: 0.1rem;
  }
  .cropped-img{
    width: 45px;
    height: 46px;
    overflow: hidden;
    text-align: center;
  }
  .indications img{
    object-position: 10px 10px;
    object-fit: left top;
  }
  }
}
.img-logo{
  height: 40px;
  span{
    font-weight: 800;
  }
  img{
    margin-right: 10px;
    height: 100%;
  }
}
.yourInput{
  width: 45%;
}
.form-group{
  margin-bottom:20px;
}
</style>