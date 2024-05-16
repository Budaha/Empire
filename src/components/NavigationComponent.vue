<template>
  <div class="navigation">
    <div class="image">
      <img class="image__first" src="../assets/img/nav/firstNav.png" />
      <img class="image__second" src="../assets/img/nav/secondNav.png" />
    </div>
    <ul class="service">
      <li @click="scrollBlock('home')">Home</li>
      <li @click="scrollBlock('aboutus')">About us</li>
      <li @click="scrollBlock('ourservices')">Our Services</li>
      <li @click="scrollBlock('ourteam')">Our Team</li>
      <li @click="scrollBlock('footer')">Contact us</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "navigationComponent",
  data() {
    return {};
  },
  methods: {
    scrollBlock(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
        block: "center",
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.image {
  position: relative;
  &__second {
    padding-top: 10px;
    padding-left: 21px;
  }
  img {
    position: absolute;
    margin-left: 145px;
    pointer-events: none;
  }
}
.service {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  li {
    cursor: pointer;
    padding-top: 23px;
    padding-right: 38px;
    font-size: 18px;
    font-weight: 600;
    line-height: 27px;
    color: #ffffff;
    font-family: "Poppins";
    &:last-child {
      margin-right: 118px;
    }
  }
}
</style>