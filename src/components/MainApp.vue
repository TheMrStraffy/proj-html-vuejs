<script>
import BusinessFeaturesMainVue from './mainComponents/BusinessFeaturesMain.vue'
import ContactTeamMainVue from './mainComponents/ContactTeamMain.vue'
import LatestPostsMainVue from './mainComponents/LatestPostsMain.vue'
import OnlineMarketingMainVue from './mainComponents/OnlineMarketingMain.vue'
import SalesTricksMainVue from './mainComponents/SalesTricksMain.vue'
import TestimonialsMainVue from './mainComponents/TestimonialsMain.vue'

export default {
  name: "MainApp",
  components:{
    OnlineMarketingMainVue, SalesTricksMainVue,
    BusinessFeaturesMainVue, TestimonialsMainVue,
    LatestPostsMainVue, ContactTeamMainVue
  }
}
</script>
<template>
  <main>
    <OnlineMarketingMainVue/>
    <SalesTricksMainVue/>
    <BusinessFeaturesMainVue/>
    <TestimonialsMainVue/>
    <LatestPostsMainVue/>
    <ContactTeamMainVue/>
  </main>
</template>


<style lang="scss" scoped>

</style>