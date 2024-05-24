<template>
  <div class="navigation">
    <div class="image">
      <img class="image__first" src="../assets/img/nav/firstNav.png" />
      <img class="image__second" src="../assets/img/nav/secondNav.png" />
    </div>
    <ul class="service">
      <div class="service__nav" v-for="(nav, index) in navs" :key="index">
        <li @click="scrollBlock(nav.id)">{{ nav.name }}</li>
      </div>
    </ul>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "navigationComponent",
  setup() {
    const navs = ref([
      {
        id: "home",
        name: "Home",
      },
      {
        id: "aboutus",
        name: "About us",
      },
      {
        id: "ourservices",
        name: "Our Services",
      },
      {
        id: "ourteam",
        name: "Our Team",
      },
      {
        id: "footer",
        name: "Contact us",
      },
    ]);
    const scrollBlock = (id) => {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
        block: "center",
      });
    };
    return {
      navs,
      scrollBlock,
    };
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
    user-select: none;
  }
}
.service {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  &__nav {
    &:last-child {
      margin-right: 117px;
    }
  }
  li {
    cursor: pointer;
    padding-top: 23px;
    padding-right: 38px;
    font-size: 18px;
    font-weight: 600;
    line-height: 27px;
    color: #ffffff;
    font-family: "Poppins";
  }
  li:hover {
    color: #ef7b3e;
  }
}
</style>