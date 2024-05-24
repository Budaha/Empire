<template>
  <div class="about-section">
    <div class="about-section__image">
      <img src="../assets/img/about/image.png" />
      <h1 class="about-section__title-img">HIGH Quality</h1>
      <div class="about-section__text-img"><p>FBA Prep Services</p></div>
    </div>
    <div class="about-section__info">
      <div class="block-name">
        <div class="line" />
        <h3 class="name">about us</h3>
      </div>
      <h1 class="title">WHAT WE DO</h1>
      <h4 class="descr">
        Empire FBA Prep Services In USA &Canada specializes in providing world
        class prep solutions for your Amazon FBA business.
      </h4>
      <div class="about-section__info-grid">
        <div class="element" v-for="(element, index) in elements" :key="index">
          <img :src="element.img" />
          <div class="text">
            <h1>{{ element.title }}</h1>
            <p>{{ element.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import grid1 from "../assets/img/about/grid1.png";
import grid2 from "../assets/img/about/grid2.png";
import grid3 from "../assets/img/about/grid3.png";
export default {
  name: "aboutusComponent",
  setup() {
    const elements = ref([
      {
        id: 1,
        img: grid1,
        title: "RECEIVE YOUR INVENTORY",
        description:
          "Send your products, packaging and inserts directly to one of our three locations strategically located in California, New York or Toronto Canada",
      },
      {
        id: 2,
        img: grid2,
        title: "PREP AND LABEL",
        description:
          "Our team will inspect all items before carefully wrapping, adding inserts, packing and attaching all the necessary labels required for delivery and receipt by Amazon",
      },
      {
        id: 3,
        img: grid3,
        title: "SHIP TO AMAZON",
        description:
          "Our staff of trained experts will complete your shipping plan, arrange pickup and delivery directly to your assigned Amazon fulfillment center",
      },
    ]);
    return {
      elements,
    };
  },
};
</script>

<style lang="scss" scoped>
.about-section {
  display: flex;
  padding-top: 108px;
  &__image {
    position: relative;
    max-width: 650px;
    pointer-events: none;
    user-select: none;
    img {
      padding-left: 11px;
    }
  }
  &__title-img {
    max-width: 150px;
    position: absolute;
    right: 60px;
    top: 98px;
    text-align: center;
    font-size: 38px;
    font-weight: 700;
    font-family: "Poppins";
    line-height: 45px;
    color: #ffffff;
  }
  &__text-img {
    p {
      max-width: 150px;
      position: absolute;
      right: 72px;
      top: 192px;
      font-family: "Lato";
      font-size: 16px;
      line-height: 25px;
      color: #ffffff;
    }
  }
  &__info {
    margin-left: 85px;
    .line {
      width: 46px;
      border-bottom: 2px solid #ef7b3e;
      margin-bottom: 7px;
    }
    .block-name {
      display: flex;
    }
    .name {
      font-weight: 700;
      font-size: 18px;
      line-height: 27px;
      color: #ef7b3e;
      font-family: "Poppins";
      text-transform: uppercase;
      padding-top: 8px;
    }
    .title {
      font-size: 40px;
      font-weight: 700;
      line-height: 60px;
      color: #313131;
      font-family: "Poppins";
      margin-top: 24px;
    }
    .descr {
      font-weight: 500;
      font-size: 15px;
      line-height: 25px;
      font-family: "Lato";
      color: #050505;
      margin-top: 7px;
      max-width: 500px;
    }
  }
  &__info-grid {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    max-width: 545px;
    .element {
      display: flex;
      border-bottom: 2px solid #ececec;
      align-items: center;
      justify-content: center;
      margin-bottom: 21px;
      &:first-child {
        margin-top: 70px;
      }
      img {
        pointer-events: none;
        user-select: none;
      }
    }
    .text {
      padding-left: 18px;
      h1 {
        font-size: 20px;
        font-weight: 700;
        line-height: 25px;
        font-family: "Poppins";
        color: #000000;
        text-transform: uppercase;
      }
      p {
        font-size: 15px;
        font-weight: 400;
        line-height: 22px;
        font-family: "Lato";
        color: #050505;
        padding-top: 4px;
        padding-bottom: 22px;
      }
    }
  }
}
</style>