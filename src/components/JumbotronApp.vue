<script>
export default {
  
  name: "JumbotronApp"
}
</script>
<template>
<div class="jumbotron">
  <div class="bgJumb"></div>
    <div class="row align-items-center h-100">
      <div class="col text">
        <h2>The biggest platform for your growth.</h2>
        <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form</p>
        <button class="mc-btn"> Read More</button>
      </div>
      <div class="col d-flex align-items-end h-100">
        <img src="src/assets/img/27-1.png" alt="">
      </div>
    </div>
  </div>
  
</template>


<style lang="scss" scoped>
.jumbotron{
  position: relative;
  min-height: 530px;
  margin-bottom: 125px;
  .bgJumb{
    position: absolute;
    z-index: -1;
    width: 100%;
    height: 95%;
    background-color: #F2F7FF;
  }
}
img{
  margin-top: 80px;
}
.text{
  margin-left: 55px;
}
h2{
  font-size: 3.5rem;
  line-height: 6rem;
}
p{
  font-size: 1.25rem;
  margin: 40px 0;
  color: #8E989F;
}
.mc-btn{
  width: 135px;
  height: 45px;
  font-size: 800;
  color: white;
  background-color: #377DFF;
  border: none;
  border-radius: 10px;
  transition: all 0.6s linear;
  &:hover{
    background-color: #1E1E1E;
  }
}
</style>