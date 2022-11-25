<script>
export default {
  name: "SalesTricksMain"
}
</script>
<template>
  <section>
    <div class="row justify-content-center">
      <div class="col">
        <h2 class="mb-3 w-75">Get tips tricks on how to skyrocket your sales.</h2>
        <p class=" w-75 text-area">Faff about only a quid blower i don't want no agro bleeding chimney pot burke tosser cras nice one boot fanny.!</p>
        <div class="box">
          <div class="row">
            <div class="col-2 ">
          <img src="../../assets/img/510.png" alt="Analysis">
            </div>
            <div class="col-10">
          <h5>Reporting Analysis</h5>
          <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout</p>
            </div>
          </div>
        </div>
        <div class="box">
          <div class="row">
            <div class="col-2">
              <img src="../../assets/img/511.png" alt="Analysis">
            </div>
            <div class="col-10">
              <h5>Technical SEO Audit</h5>
              <p>It is a long established fact that a reader will be distracted     by the readable content of a page when looking at its layout</p>
            </div>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="img-box">
          <img src="../../assets/img/509.jpeg" alt="">
        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
section{
  margin-bottom: 140px;
}
p{
  color: #8E989F;
}
.text-area{
  margin-bottom: 60px;
}
.box{
  cursor: pointer;
  margin-bottom: 20px;
  transition: all 0.5s linear;
  &:hover{
      color: #377DFF;
    box-shadow: 10px 9px 30px -7px rgba(79,79,79,0.59);
  -webkit-box-shadow: 10px 9px 30px -7px rgba(79,79,79,0.59);
  -moz-box-shadow: 10px 9px 30px -7px rgba(79,79,79,0.59);
  }
}
</style>