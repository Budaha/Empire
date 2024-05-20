<template>
  <div class="footer-section">
    <div class="footer-section__block-grid">
      <div class="first-block">
        <h1 class="title" @click="scrollBlock('header')">
          <span>LOGO</span> HERE
        </h1>
        <p class="descr">
          USA & Canada specializes in providing world class prep solutions for
          your Amazon FBA business.
        </p>
        <button class="btn">Book Now</button>
      </div>
      <div class="first-block">
        <h1 class="title--1">QUICK LINKS</h1>
        <ul class="arrow">
          <div class="arrow--1" v-for="(arrow, index) in arrows" :key="index">
            <img :src="arrow.img" />
            <li @click="scrollBlock(arrow.id)">{{ arrow.name }}</li>
          </div>
        </ul>
      </div>
      <div class="first-block">
        <h1 class="title--1">OUR SERVICES</h1>
        <ul>
          <div class="flex">
            <img src="../assets/img/header/phone.png" />
            <li>1 (877) 618-0069</li>
          </div>
          <div class="flex">
            <img src="../assets/img/header/email.png" />
            <li>info@empireprepservices.com</li>
          </div>
          <div class="flex">
            <img src="../assets/img/header/address.png" />
            <li>California: 4010 Valley Blvd Ste 108, Walnut, CA 91789</li>
          </div>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import arrow from "../assets/img/footer/arrow.png";
export default {
  name: "footerComponent",
  setup() {
    const scrollBlock = (id) => {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
        block: "center",
      });
    };
    const arrows = ref([
      {
        id: "home",
        img: arrow,
        name: "Home",
      },
      {
        id: "aboutus",
        img: arrow,
        name: "About us",
      },
      {
        id: "ourservices",
        img: arrow,
        name: "Our Services",
      },
      {
        id: "ourteam",
        img: arrow,
        name: "Our Team",
      },
      {
        id: "footer",
        img: arrow,
        name: "Contact us",
      },
    ]);
    return {
      scrollBlock,
      arrows,
    };
  },
};
</script>

<style lang="scss" scoped>
.footer-section {
  display: flex;
  justify-content: center;
  &__block-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    max-width: 1440px;
    margin-top: 80px;
    .first-block {
      margin-left: 110px;
      display: flex;
      flex-direction: column;
      &:last-child {
        margin-left: 13px;
      }
      .title--1 {
        text-transform: uppercase;
        font-weight: 700;
        color: #ffffff;
        font-size: 20px;
        margin-top: 20px;
      }
      .arrow {
        display: flex;
        flex-direction: column;
        margin-top: 14px;
      }
      .arrow--1 {
        display: flex;
        align-items: center;
        img {
          width: 5px;
          height: 5px;
        }
      }
      li {
        font-family: "Poppins";
        font-size: 16px;
        font-weight: 400;
        line-height: 27px;
        color: #ffffff;
        margin-left: 19px;
        cursor: pointer;
        &:first-child {
          margin-top: 14px;
        }
      }
      li:hover {
        color: #ef7b3e;
      }
      .flex {
        display: flex;
        max-width: 300px;
        cursor: pointer;
        &:first-child {
          margin-top: 11px;
        }
        img {
          width: 15px;
          height: 17px;
          &:first-child {
            margin-top: 20px;
          }
        }
        li {
          margin-top: 18px;
          font-family: "Lato";
          font-size: 16px;
          font-weight: 600;
          line-height: 19.2px;
        }
      }
    }
    .title {
      text-transform: uppercase;
      font-weight: 700;
      color: #ffffff;
      font-size: 40px;
      cursor: pointer;
      span {
        font-weight: 500;
        font-size: 27px;
      }
    }
    .descr {
      font-family: "Lato";
      font-size: 16px;
      font-weight: 400;
      line-height: 19.2px;
      text-align: left;
      color: #ffffff;
      margin-top: 12px;
      max-width: 345px;
    }
    .btn {
      width: 161px;
      height: 45px;
      border-radius: 35px;
      border: 1px solid #ef7b3e;
      background: #2e2e2e;
      font-family: "Poppins";
      font-size: 16px;
      font-weight: 600;
      line-height: 24px;
      color: #ef7b3e;
      margin-top: 25px;
      cursor: pointer;
    }
  }
}
</style>