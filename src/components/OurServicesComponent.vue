<template>
  <div class="ourservice-section">
    <div class="ourservice-section__text">
      <h1 class="ourservice-section__title"><span>OUR</span> SERVICES</h1>
      <p class="ourservice-section__info">
        Our Services: Empire FBA Prep Services In USA &amp; Canada specializes
        in providing world class prep solutions for your Amazon FBA business.
        Whether you are new to Amazon or need a 3rd party logistics specialist
        to help scale your growing business we have solutions to meet all of
        your FBA prep needs large or small.
      </p>
    </div>
    <div class="ourservice-section__service">
      <div class="cards" v-for="(card, index) in cards" :key="index">
        <img :src="card.img" />
        <h1 class="title">{{ card.title }}</h1>
        <p class="descr">{{ card.description }}</p>
        <button class="btn"><p>READ MORE</p></button>
      </div>
    </div>
  </div>
</template>
  
  <script>
import { ref } from "vue";
import labeling from "../assets/img/ourservices/labeling.png";
import bubble from "../assets/img/ourservices/bubble.png";
import bundling from "../assets/img/ourservices/bundling.png";
export default {
  name: "ourServicesComponent",
  setup() {
    const cards = ref([
      {
        id: 1,
        img: labeling,
        title: "Labeling",
        description:
          "Every unit, carton and pallet will be labeled by us as required. Rest easy knowing your shipments will arrive at their designated fulfillment centers as scheduled and on time",
      },
      {
        id: 2,
        img: bubble,
        title: "Bubble Wrap",
        description:
          "It’s crucial for inventory to arrive in pristine condition. All items will be carefully bubble wrapped and poly bagged as necessary to guarantee safe delivery",
      },
      {
        id: 3,
        img: bundling,
        title: "BUNDLING",
        description:
          "You’ve built the perfect bundle for your customers and every detail counts. Bundles will be packed by us according to current specifications as required by Amazon",
      },
    ]);
    return {
      cards,
    };
  },
};
</script>
  
  <style lang="scss" scoped>
.ourservice-section {
  &__text {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  &__title {
    font-size: 40px;
    font-weight: 700;
    line-height: 60px;
    font-family: "Poppins";
    color: #ffffff;
    text-align: center;
    padding-top: 76px;
    span {
      text-decoration: underline;
      text-underline-offset: 9px;
      text-decoration-thickness: 2px;
      text-decoration-color: #ef7b3e;
    }
  }
  &__info {
    max-width: 895px;
    padding-top: 9px;
    font-size: 16px;
    font-weight: 500;
    line-height: 21px;
    font-family: "Lato";
    color: #ffffff;
  }
  &__service {
    display: flex;
    .cards {
      max-width: 362px;
      height: 374px;
      background: #ffffff;
      border-radius: 10px;
      margin-top: 154px;
      display: flex;
      flex-direction: column;
      margin-left: 28px;
      box-shadow: 0px 0px 35px 15px #0000001a;
      &:first-child {
        margin-left: 147px;
      }
      img {
        margin-top: -111px;
        padding: 14px;
        pointer-events: none;
      }
      .title {
        font-family: "Poppins";
        font-size: 24px;
        line-height: 21px;
        color: #2e2e2e;
        text-align: center;
        margin-top: 18px;
      }
      .descr {
        font-family: "Lato";
        font-size: 15px;
        line-height: 28px;
        color: #050505;
        text-align: center;
        padding: 20px 30px;
      }
      .btn {
        padding-top: 2px;
        background: none;
        border: none;
        cursor: pointer;
        p {
          font-size: 14px;
          font-weight: 600;
          line-height: 21px;
          font-family: "Poppins";
          color: #ef7b3e;
          text-decoration: underline;
          text-underline-offset: 3px;
          text-decoration-thickness: 1px;
          text-decoration-color: #ef7b3e;
        }
      }
    }
  }
}
</style>