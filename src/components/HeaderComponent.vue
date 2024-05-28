<template>
  <div class="contacts">
    <div class="navbar">
      <div class="address">
        <img src="../assets/img/header/address.png" />
        <a
          class="address__text"
          href="https://www.google.com/maps?ll=34.038973690169456, -117.82229369628088"
          target="_blank"
          >California: 4010 Valley Blvd Ste 108, Walnut, CA 91789</a
        >
      </div>
      <div class="email">
        <img src="../assets/img/header/email.png" />
        <a class="email__text" href="mailto:info@empireprepservices.com"
          >info@empireprepservices.com</a
        >
      </div>
      <div class="phone">
        <img src="../assets/img/header/phone.png" />
        <a class="phone__text" href="tel:1 (877) 618-0069">1 (877) 618-0069</a>
      </div>
      <button class="btn">Book Now</button>
    </div>
    <img
      src="../assets/img/header/menu.svg"
      class="menubtn"
      @click="openMenu"
    />
    <!-- menu -->
    <div class="menu" v-if="isMenu">
      <img
        src="../assets/img/header/close.svg"
        class="menu__close"
        @click="closeMenu"
      />
      <ul class="menu__service">
        <div
          class="menu__service-nav"
          v-for="(nav, index) in navs"
          :key="index"
        >
          <li @click="scrollBlock(nav.id)">{{ nav.name }}</li>
        </div>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
// data
const isMenu = ref(false);
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
// methods
const openMenu = () => {
  isMenu.value = true;
};
const closeMenu = () => {
  if (!isMenu.value) return;
  isMenu.value = false;
};
const scrollBlock = (id) => {
  document.getElementById(id).scrollIntoView({
    behavior: "smooth",
    block: "center",
  });
};
document.addEventListener("keydown", (e) => {
  if (e.keyCode == 27) {
    isMenu.value = false;
  }
});
window.addEventListener("click", (e) => {
  const target = e.target;
  if (!target.closest(".menu") && !target.closest(".menubtn") && isMenu.value) {
    isMenu.value = false;
  }
});
window.addEventListener("scroll", () => {
  const scrollPosition = document.documentElement.scrollTop;
  if (scrollPosition >= 120 && isMenu.value) {
    isMenu.value = false;
    // console.log(scrollPosition);
  }
});
</script>

<style lang="scss" scoped>
.contacts {
  display: flex;
  justify-content: flex-end;
  max-width: 1440px;
  @media (max-width: 1440px) {
    justify-content: center;
  }
  @media (max-width: 1200px) {
    justify-content: flex-end;
  }
  .navbar {
    display: flex;
    @media (max-width: 1200px) {
      display: none;
    }
    .address {
      display: flex;
      gap: 8px;
      align-items: center;
      margin-right: 40px;
      &__text {
        font-weight: 400;
        font-size: 16px;
        line-height: 19.2px;
        color: #313131;
        font-family: "Lato";
        text-decoration: none;
      }
    }
    .email {
      display: flex;
      gap: 8px;
      align-items: center;
      margin-right: 25px;
      &__text {
        font-weight: 400;
        font-size: 16px;
        line-height: 19.2px;
        color: #313131;
        font-family: "Lato";
        text-decoration: none;
      }
    }
    .phone {
      display: flex;
      align-items: center;
      margin-right: 40px;
      gap: 8px;
      &__text {
        font-weight: 600;
        font-size: 16px;
        line-height: 19.2px;
        color: #313131;
        font-family: "Lato";
        text-decoration: none;
      }
    }
    img {
      width: 15px;
      height: 15px;
      user-select: none;
      pointer-events: none;
    }
    p {
      cursor: pointer;
    }
    a:hover {
      color: #ef7b3e;
    }
    .btn {
      cursor: pointer;
      width: 161px;
      height: 45px;
      border-radius: 35px;
      background: #ef7b3e;
      border: none;
      margin-right: 146px;
      margin-top: 4px;
      color: #ffffff;
      font-weight: 600;
      font-size: 16px;
      line-height: 10px;
      font-family: "Poppins";
      @media (max-width: 1440px) {
        margin-right: 0;
      }
    }
    .btn:hover {
      background: #515151;
    }
  }
  .menubtn {
    display: none;
    width: 40px;
    height: 40px;
    @media (max-width: 1200px) {
      display: flex;
      margin-top: 3px;
      margin-right: 20px;
      cursor: pointer;
    }
  }
  .menu {
    position: fixed;
    top: 0;
    right: 0;
    width: 400px;
    height: auto;
    background: #313131;
    z-index: 1;
    padding: 20px;
    @media (max-width: 500px) {
      width: 100%;
      padding: 20px 0;
    }
    &__close {
      cursor: pointer;
      position: absolute;
      top: 10px;
      right: 20px;
      font-size: 40px;
      width: 40px;
      height: 40px;
    }
    &__service {
      margin-top: 30px;
      @media (max-width: 500px) {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
    }
    &__service-nav {
      margin-top: 10px;
      li {
        font-size: 18px;
        font-weight: 600;
        line-height: 27px;
        font-family: "Poppins";
        color: #ffffff;
        cursor: pointer;
      }
      li:hover {
        color: #ef7b3e;
      }
    }
  }
}
</style>