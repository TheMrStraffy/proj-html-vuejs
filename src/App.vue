<script>
import FooterAppVue from './components/FooterApp.vue'
import HeaderAppVue from './components/HeaderApp.vue'
import JumbotronAppVue from './components/JumbotronApp.vue'
import MainAppVue from './components/MainApp.vue'

export default{
  name: "App",
  components: {
    HeaderAppVue, JumbotronAppVue,
    MainAppVue, FooterAppVue, 
    }
 }
</script>

<template>
<div class="container">
  <HeaderAppVue/>
  <JumbotronAppVue/>
  <MainAppVue/>
  <FooterAppVue/>
</div>
</template>

<style lang="scss">
@import './styles/generals.scss';
</style>
