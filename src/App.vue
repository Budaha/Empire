<template>
  <div class="header">
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
</template>
<script>
import headerComponent from "@/components/HeaderComponent.vue";
import navigationComponent from "@/components/NavigationComponent.vue";
import homeComponent from "@/components/HomeComponent.vue";
import aboutusComponent from "@/components/AboutusComponent.vue";
export default {
  components: {
    headerComponent,
    navigationComponent,
    homeComponent,
    aboutusComponent,
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
}
</style>
