<template>
  <div class="header" id="header">
    <headerComponent class="container" />
  </div>
  <div class="nav">
    <navigationComponent class="container" />
  </div>
  <div class="home" id="home">
    <homeComponent class="container" />
  </div>
  <div class="aboutus" id="aboutus">
    <aboutusComponent class="container" />
  </div>
  <div class="our-services" id="ourservices">
    <ourServicesComponent class="container" />
  </div>
  <div class="stages">
    <stagesComponent class="container" />
  </div>
  <div class="our-team" id="ourteam">
    <ourTeamComponent class="ourteam" />
  </div>
  <div class="footer" id="footer">
    <footerComponent />
  </div>
  <div class="bottom">
    <bottomComponent />
  </div>
</template>
<script>
import headerComponent from "@/components/HeaderComponent.vue";
import navigationComponent from "@/components/NavigationComponent.vue";
import homeComponent from "@/components/HomeComponent.vue";
import aboutusComponent from "@/components/AboutusComponent.vue";
import ourServicesComponent from "@/components/OurServicesComponent.vue";
import stagesComponent from "@/components/StagesComponent.vue";
import ourTeamComponent from "./components/OurTeamComponent.vue";
import footerComponent from "@/components/FooterComponent.vue";
import bottomComponent from "@/components/BottomComponent.vue";
export default {
  components: {
    headerComponent,
    navigationComponent,
    homeComponent,
    aboutusComponent,
    ourServicesComponent,
    stagesComponent,
    ourTeamComponent,
    footerComponent,
    bottomComponent,
  },
};
</script>
<style lang="scss">
.header {
  background: #ffffff;
  padding-top: 8px;
  padding-bottom: 9px;
}
.nav {
  background: #313131;
  padding-bottom: 24px;
}
.home {
  background: #ef7b3e;
  padding-bottom: 172px;
}
.aboutus {
  background: #ffffff;
  margin-bottom: -4px;
}
.our-services {
  background: url(/src/assets/img/ourservices/ourservice.png);
}
.stages {
  background: #ffffff;
  margin-top: -76px;
  padding-bottom: 71px;
}
.our-team {
  background: #ef7b3e;
  padding-bottom: 104px;
}
.footer {
  background: #2e2e2e;
  padding-bottom: 100px;
  border-bottom: 1px solid #ffffff;
}
.bottom {
  background: #2e2e2e;
  padding-bottom: 20px;
}
</style>
